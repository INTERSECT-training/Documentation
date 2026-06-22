---
title: "Documentation in Practice"
teaching: 8
exercises: 14
---

::::::::::::::::::::::::::::::::::::::: objectives

- Become familiar with real-life examples of documentation.
- Practice writing different kinds of documentation.
- Understand the role of the README, docstrings, and citation/licensing files.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What does developer documentation look like in practice?
- What does user documentation look like in practice?
- What belongs in a README, a docstring, and a citation file?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Start the Right Way: the README

Before any framework or tool, almost every project's documentation begins with a single
file: the **README**. It's the first thing a visitor sees on GitHub, and for many research
projects it's the *only* documentation that exists. A good README answers a newcomer's
questions fast:

| Section | Answers |
|---------|---------|
| **What and why** | What does this do, and why would I use it? |
| **Install** | How do I get it running? |
| **Usage / quick example** | Show me the simplest thing that works. |
| **License** | Can I use it, and how? |
| **How to cite** | How do I give credit in a paper? |
| **Contributing / contact** | How do I report a bug or get help? |

You don't need all of these on day one — but a README that covers *what/why* and a *quick
example* already puts you ahead of most research code.

## Document the *Why*, Not the *What*: Docstrings and Comments

Two kinds of in-code documentation do most of the day-to-day work:

- **Docstrings** describe *what a function/class does and how to use it* — its inputs,
  outputs, and behavior. They're written for the person *calling* your code (and power tools
  like Sphinx, covered next episode).
- **Inline comments** explain *why* a particular piece of code is the way it is — the
  non-obvious decision, the workaround, the edge case.

The better practice: **comment the *why*, not the *what***. Code already says *what* it does;
a comment like `# add 1 to i` is noise. A comment explaining *why* you add 1 (an off-by-one
in an upstream API, say) is gold.

## Developer Documentation Examples

| Documentation Type | Explanation | Example |
| ------------------ | ----------- | ------- |
| Team processes | This type of documentation documents the expected development processes within a team. These generally include an objective, stakeholders, and steps to follow. | [US-RSE'23 Website Repository `CONTRIBUTING` guide](https://github.com/USRSE/usrse23/blob/main/CONTRIBUTING.md) |
| Styles and standards | This type of documentation states the expectations on styles and standards within a code. This can include preferred tools, usage of existing style guides, and project or domain-specific standards. | [Pyomo's Required Coding Standards](https://pyomo.readthedocs.io/en/stable/contribution_guide.html#coding-standards) |
| API | This type of documentation is both developer and user documentation. From a developer perspective, this documentation elaborates the intent of the code, e.g., what the code is supposed to be doing, which can improve maintainability. | [Spack's API Documentation](https://spack.readthedocs.io/en/latest/spack.html) |

:::::::::::::::::::::::::::::::::::::::  challenge

## PRACTICE: Euler's Method Documentation

Have you heard of Euler's Method? It's a way to calculate a numerical
approximation for the value of a function, based on a starting value `x_0`,
a particular step size `h`, and the derivative of the function.

Write some documentation for the following code snippet:

```python
class EulersMethod:
    def deriv(self, x, y):
        return y**2 + y*x + x**3
    def approx(self, y, x, h):
        y_j = y + h*self.deriv(x, y)
        x_j = x + h
        return y_j, x_j
```

**Bonus**: How would you improve this code to make it more clear?

**GenAI Bonus**: Ask an LLM to write a docstring for this class. Then *critique* its output:
Did it correctly describe what `deriv` and `approx` actually do? Did it invent behavior the
code doesn't have? Did it explain the *why*? Fix what it got wrong. This is the review skill
that matters most when documenting with AI.

::::::::::::::::::::::::::::::::::::::::::::::::::

## User Documentation Examples

| Documentation Type | Explanation | Example |
| ------------------ | ----------- | ------- |
| Installation | This documentation is meant to help users get a package installed and working properly. Frequently, it will detail not only the different methods of installing the software, but also simple explanations of how to ensure it was installed correctly (e.g., a sanity test).  | [NumPy Installation Instructions](https://numpy.org/install/) |
| Debugging and troubleshooting | This type of documentation helps users troubleshoot common errors. This is normally built from previous questions or common mistakes, such as invalid setup, options, or inputs. | [Pyomo Common Warnings and Errors](https://pyomo.readthedocs.io/en/stable/errors.html) |
| Tutorials and examples | This type of documentation is meant to show users, step-by-step, on either small or real-world scales, how a software package is supposed to be used. This documentation helps with clarifying the developers' intended use and acts as a starting point for users. | [Pandas Getting Started Tutorials](https://pandas.pydata.org/docs/getting_started/intro_tutorials/index.html) |

:::::::::::::::::::::::::::::::::::::::  challenge

## PRACTICE: Install Python

Assume that you have a new team member who does not have Python on their
machine and wants to install it. They send you an email to ask how they
should do it.

* Do you have all the information you need to answer this question? Why or why not?
* Given only the email, write instructions detailing how to install Python from python.org.

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::  callout

## REMINDER: Culture, Context, Experience

Keep in mind culture, context, and experience when writing your instructions.

:::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::  callout

## Make It Citable: CITATION and LICENSE

Two small files matter a lot for *research* software:

- **`LICENSE`** tells others what they're legally allowed to do with your code. Without one,
  the default is "all rights reserved" — others can't reuse it, even if your repo is public.
- **`CITATION.cff`** is a simple, structured ([Citation File Format](https://citation-file-format.github.io/))
  file telling people how to cite your software. GitHub reads it and shows a "Cite this
  repository" button automatically — so your work gets credited correctly in papers.

These pair naturally with the contributing guides and pull-request workflow from the previous
session. (INTERSECT's own lesson repos include both.)

:::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- There are numerous examples of different types of documentation in practice, each with its own intended purpose.
- A project must pick the documentation that makes the most sense for its use case and domain.
- The README is the front door; docstrings document the *why*; LICENSE and CITATION.cff make research software reusable and citable.
- GenAI can draft documentation quickly, but you must review it for accuracy.

::::::::::::::::::::::::::::::::::::::::::::::::::

