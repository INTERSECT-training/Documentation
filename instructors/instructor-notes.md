---
title: 'Instructor Notes'
---

## Timing and Schedule

This lesson is designed for a **single 90-minute slot**. It is taught *after* the
collaborative-git section (issues, branches, pull requests), so learners already know how to
branch, commit, and push — you can move briskly through anything git-related.

| Time | Episode | Notes |
|------|---------|-------|
| ~10 min | **Introduction** | Benefits/challenges tables + Spack browsing challenge. Seeds the genAI theme. |
| ~12 min | **Types of Software Documentation** | Dev/user split + the new **Diátaxis** four-mode lens. |
| ~28 min | **Documentation Better Practices** | The two **sandwich exercises** are the heart of the lesson — protect this time. |
| ~22 min | **Documentation in Practice** | README, docstrings ("why not what"), CITATION/licensing, and the Euler's Method practice (with genAI twist). |
| ~18 min | **Documentation Tools** | Style guides, Sphinx quickstart, and publishing. |

Total ~90 min.

### The Optional Tools exercise

The final Tools exercise is intentionally **optional / take-home** — learners almost certainly
won't finish it live, and that's by design. If you're short on time, point them to it and move
on; do **not** cut the sandwich exercises to make room.

It now offers two paths:

- **Option A — a personal website** (`YOURUSERNAME.github.io` from an academic/personal
  template). This is the recommended long-term takeaway: most learners will get more lasting
  value from a CV/portfolio site than from publishing the practice docs. The instructor having
  their own such site to show off is a great motivator.
- **Option B — publish the Sphinx docs** via Read the Docs or GitHub Pages Actions, for those
  who want to close the loop on the project-docs workflow.

### GenAI

GenAI is woven through the whole lesson rather than tacked on at the end:

- **Introduction** — sets up "AI makes drafts cheap; the bottleneck moves to review."
- **Better Practices** — ties LLM hallucination to the sandwich "benefit of context" point.
- **Practice** — the Euler's Method exercise has a step to draft a docstring with an LLM and
  then critique/correct it.
- **Tools** — AI assistants (Copilot, IDE docstring generators) with verify-it and
  data-policy caveats.

Reinforce the through-line: **generate with AI, but always review.**

## Exercise Notes

- **Sandwich (x2):** The point is discovering one's own *bias / benefit of context*. The
  second pass should be visibly more detailed than the first — that contrast is the lesson.
- **Euler's Method:** Used in both Practice (free-form docs) and Tools (Google-style
  docstring). Learners can build on their first attempt.
- **Sphinx quickstart:** Have learners use a virtual environment; default quickstart options
  are fine. This is the input to the optional publishing step.
