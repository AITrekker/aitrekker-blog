---
layout: post
title: "Running Old and New Model Versions Without Doubling the GPU Bill"
date: 2026-11-22 09:00:00 -0800
---

Your models get better every week with new data, more fine-tuning and another RL run, but you can't run to Best Buy for a few more Blackwells every time a new checkpoint needs GPUs. The shiny new model competes with the tried and true one for the same capacity, and while some teams want it right away, others serve customer traffic on the old model and want it left alone.

I lead a platform team that runs a large fleet for LLM training and inference across 25+ regions. Running old and new versions side by side without doubling the GPU bill takes six versioning practices.

<!--more-->

## 1. Immutable version IDs

An ID like `support-summarizer-2026-11-15` always refers to the same weights, tokenizer, chat template, engine version and quantization. A vLLM upgrade can shift outputs as much as new weights do, so an engine change gets a new ID too.

## 2. Aliases for teams that want to move

A prototype can follow `support-summarizer-stable` and pick up every promoted release, while a customer-facing workflow pins the dated ID and upgrades on its own schedule. When a pinned ID retires, return an error, since silent forwarding to the new model recreates the problem.

## 3. Routing by model name

Callers use a model name, and a gateway maps it to whatever serves it. Team A can stay on the current build while Team B canaries the next build on 5% of traffic, and a rollback becomes a config change.

## 4. Cheap old versions

Five fine-tunes with three supported versions each add up to 15 deployments, and on dedicated GPU endpoints the support policy turns into a budget argument. SageMaker inference components let versions share GPUs and scale separately, and if the fine-tunes are LoRA adapters on one base model, all 15 can run on one fleet.

## 5. Rollouts that work like code deploys

Mirror production traffic to the candidate and compare outputs before callers see them. Then shift traffic in small batches with alarms that trigger automatic rollback. SageMaker's rolling updates for inference components handle the batching and rollback.

## 6. A report for each team on what changed

Each team registers a few hundred real prompts, every candidate runs against all of them, and each team gets its own report before promotion. Of the six, this one does the most to ease reluctance, since teams can review the change like any other dependency update.

The first three cost little before the first team adopts and a lot to retrofit afterward, so they should be baked in the platform early.
