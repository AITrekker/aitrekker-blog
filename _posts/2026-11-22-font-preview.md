---
layout: post
title: "Font preview: four options"
date: 2026-11-22 08:00:00 -0800
---

<style>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&family=Inter:wght@400;600&family=JetBrains+Mono:wght@400;600&display=swap');
.fp { border: 1px solid rgba(127,127,127,.35); border-radius: 8px; padding: 1.2rem 1.4rem; margin: 0 0 2rem; }
.fp .lbl { font-family: var(--sans); font-size: .75rem; font-weight: 600; letter-spacing: .06em; text-transform: uppercase; opacity: .65; margin: 0 0 .8rem; }
.fp h3 { margin: 0 0 .6rem; font-size: 1.5rem; font-weight: 600; line-height: 1.25; }
.fp h4 { margin: 1.2rem 0 .4rem; font-size: 1.15rem; font-weight: 600; }
.fp p { font-size: 1.06rem; line-height: 1.65; margin: 0 0 .8rem; }
.fp code { font-size: .88em; background: rgba(127,127,127,.14); padding: .1em .35em; border-radius: 4px; }
.fp pre { font-size: .86rem; line-height: 1.55; background: rgba(127,127,127,.14); padding: .9rem 1rem; border-radius: 6px; overflow-x: auto; margin: .4rem 0 0; }
.fp pre code { background: none; padding: 0; font-size: 1em; }
</style>

Each box below sets the same excerpt in one font option: a post title, body text, a section heading, inline code, and a code block. Tell me which letter you want and I will apply it site-wide and delete this post.

<!--more-->

<div class="fp" style="font-family: 'IBM Plex Sans', sans-serif;" markdown="0">
<p class="lbl">Option A: IBM Plex Sans + IBM Plex Mono (recommended)</p>
<h3 style="font-family: 'IBM Plex Sans', sans-serif;">Running Old and New Model Versions Without Doubling the GPU Bill</h3>
<p>Your models get better every week with new data, more fine-tuning and another RL run, but you can't run to Best Buy for a few more Blackwells every time a new checkpoint needs GPUs. The shiny new model competes with the tried and true one for the same capacity.</p>
<h4 style="font-family: 'IBM Plex Sans', sans-serif;">2. Aliases for teams that want to move</h4>
<p>A prototype can follow <code style="font-family: 'IBM Plex Mono', monospace;">support-summarizer-stable</code> and pick up every promoted release, while a customer-facing workflow pins the dated ID <code style="font-family: 'IBM Plex Mono', monospace;">support-summarizer-2026-11-15</code> and upgrades on its own schedule.</p>
<pre style="font-family: 'IBM Plex Mono', monospace;"><code>routes:
  support-summarizer-stable:
    - target: support-summarizer-2026-11-15   # weight: 95
    - target: support-summarizer-2026-11-22   # weight: 5 (canary)
  0O1lI|  {} [] () =&gt; != &lt;= &gt;=</code></pre>
</div>

<div class="fp" style="font-family: 'Inter', sans-serif;" markdown="0">
<p class="lbl">Option B: Inter + JetBrains Mono</p>
<h3 style="font-family: 'Inter', sans-serif;">Running Old and New Model Versions Without Doubling the GPU Bill</h3>
<p>Your models get better every week with new data, more fine-tuning and another RL run, but you can't run to Best Buy for a few more Blackwells every time a new checkpoint needs GPUs. The shiny new model competes with the tried and true one for the same capacity.</p>
<h4 style="font-family: 'Inter', sans-serif;">2. Aliases for teams that want to move</h4>
<p>A prototype can follow <code style="font-family: 'JetBrains Mono', monospace;">support-summarizer-stable</code> and pick up every promoted release, while a customer-facing workflow pins the dated ID <code style="font-family: 'JetBrains Mono', monospace;">support-summarizer-2026-11-15</code> and upgrades on its own schedule.</p>
<pre style="font-family: 'JetBrains Mono', monospace;"><code>routes:
  support-summarizer-stable:
    - target: support-summarizer-2026-11-15   # weight: 95
    - target: support-summarizer-2026-11-22   # weight: 5 (canary)
  0O1lI|  {} [] () =&gt; != &lt;= &gt;=</code></pre>
</div>

<div class="fp" style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;" markdown="0">
<p class="lbl">Option C: System fonts (San Francisco on Mac, Segoe UI on Windows)</p>
<h3 style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;">Running Old and New Model Versions Without Doubling the GPU Bill</h3>
<p>Your models get better every week with new data, more fine-tuning and another RL run, but you can't run to Best Buy for a few more Blackwells every time a new checkpoint needs GPUs. The shiny new model competes with the tried and true one for the same capacity.</p>
<h4 style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;">2. Aliases for teams that want to move</h4>
<p>A prototype can follow <code style="font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;">support-summarizer-stable</code> and pick up every promoted release, while a customer-facing workflow pins the dated ID <code style="font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;">support-summarizer-2026-11-15</code> and upgrades on its own schedule.</p>
<pre style="font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;"><code>routes:
  support-summarizer-stable:
    - target: support-summarizer-2026-11-15   # weight: 95
    - target: support-summarizer-2026-11-22   # weight: 5 (canary)
  0O1lI|  {} [] () =&gt; != &lt;= &gt;=</code></pre>
</div>

<div class="fp" style="font-family: 'Source Serif 4', Georgia, serif;" markdown="0">
<p class="lbl">Option D: Source Serif 4 (current) + IBM Plex Mono</p>
<h3 style="font-family: 'Source Serif 4', Georgia, serif;">Running Old and New Model Versions Without Doubling the GPU Bill</h3>
<p>Your models get better every week with new data, more fine-tuning and another RL run, but you can't run to Best Buy for a few more Blackwells every time a new checkpoint needs GPUs. The shiny new model competes with the tried and true one for the same capacity.</p>
<h4 style="font-family: 'Source Serif 4', Georgia, serif;">2. Aliases for teams that want to move</h4>
<p>A prototype can follow <code style="font-family: 'IBM Plex Mono', monospace;">support-summarizer-stable</code> and pick up every promoted release, while a customer-facing workflow pins the dated ID <code style="font-family: 'IBM Plex Mono', monospace;">support-summarizer-2026-11-15</code> and upgrades on its own schedule.</p>
<pre style="font-family: 'IBM Plex Mono', monospace;"><code>routes:
  support-summarizer-stable:
    - target: support-summarizer-2026-11-15   # weight: 95
    - target: support-summarizer-2026-11-22   # weight: 5 (canary)
  0O1lI|  {} [] () =&gt; != &lt;= &gt;=</code></pre>
</div>
