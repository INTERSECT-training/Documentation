---
title: "Documentation in Practice"
teaching: 5
exercises: 10
---

::::::::::::::::::::::::::::::::::::::: objectives

- "Become familiar with real-life examples of documentation."
- "Practice writing different kinds of documentation."

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- "What does developer documentation look like in practice?"
- "What does user documentation look like in practice?"

::::::::::::::::::::::::::::::::::::::::::::::::::

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

**BONUS**: How would you improve this code to make it more clear?

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

:::::::::::::::::::::::::::::::::::::::: keypoints

- "There are numerous examples of different types of documentation in practice, each with its own intended purpose."
- "A project must pick the documentation that makes the most sense for its use case and domain."

::::::::::::::::::::::::::::::::::::::::::::::::::

