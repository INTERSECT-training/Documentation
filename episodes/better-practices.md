---
title: "Documentation Better Practices"
teaching: 10
exercises: 20
---

::::::::::::::::::::::::::::::::::::::: objectives

- Learn about some of the unconscious biases that are apparent when writing documentation.
- Become familiar with practices that have been empirically shown to improve software documentation, both in process and end product.


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How does bias affect documentation?
- What are better practices for software documentation?

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Let's make a sandwich

We are going to make a nut butter and jelly sandwich.

* Write instructions for making this sandwich.
* Trade instructions with another participant and read each others'.
* How clear are the instructions? What are the strengths and weaknesses?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Bias in Documentation

![](fig/sandwich.png){alt='Getty Images - a image displaying a cartoon rendition of a peanut butter and jelly sandwich'}

You have now told your partner how to make a sandwich. Have you ever done that before?
Maybe you told them the steps:

1. Get two slices of bread
1. Spread condiments on the bread
1. Put the slices together

These steps may seem clear to you, but you have the benefit of context. You
know what a sandwich is. You've eaten one before. You may have even made
one before. As a result, you are able to fill in the logical gaps that
someone who has never seen or eaten a sandwich might not know.

You have the **benefit of context** — and your reader may not. Be thoughtful about three
things in particular:

| Watch out for... | Because... | Better Practice |
|----------------|----------|---------|
| **Culture** | Slang and colloquialisms ("spaghetti code") don't translate. | Use clear, concise language; assume a different background. |
| **Context** | The same word ("workflow") means different things across domains. | Define domain-specific terms; don't assume shared jargon. |
| **Experience** | Readers range from novice to expert. | Match the expected experience level — and *state* that level in the docs. |

## Documentation Better Practices

There is no one-size-fits-all process. Use these as a guide for practices that tend to help:

| Practice | Why |
|----------|-----|
| **Version control your docs** | Track changes, revert, and review them just like source code — especially if docs live outside the code repo. |
| **Good enough beats perfect** | Don't get stuck polishing forever; ship useful docs and improve them later. |
| **Less is more** | Every doc is technical debt. Keep only what you need; flag the rest for removal. |
| **Know your audience** | Their knowledge level tells you what to explain and what to assume. |
| **Document as you go** | Writing it now, while it's fresh, beats reconstructing it a month later. |
| **User-test your docs** | Have a *new* person follow them; every question or snag marks a gap to fix. |

::::::::::::::::::::::::::::::::::::::::::  callout

## GenAI and the "benefit of context"

An LLM has the *opposite* problem from you: it has no real knowledge of *your* project,
domain, or users — but it will confidently fill the gaps anyway (this is **hallucination**).
That makes genAI excellent for a **first draft** and for spotting what you forgot to explain,
but the human must supply the true context and **verify every claim**. Think of it as a fast,
eager collaborator who has never actually used your software. A good rule: *generate with AI,
but you own the review.*

::::::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Let's make a sandwich... again

Try this exercise again. We want to make a nut butter and jelly sandwich.

* Write instructions to make this sandwich.
* Partner with the same participant as before.
* Discuss: What changes did you make?

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- It is important to be aware of potential unconscious biases when writing documentation. Make sure to consider culture, context, and experience.
- No single practice will fit all software projects, but there are some generally better practices: version control, less is more, know your audience, document as you go.
- GenAI can draft and gap-check documentation, but it lacks real project context — you supply the context and verify the output.

::::::::::::::::::::::::::::::::::::::::::::::::::

