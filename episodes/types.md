---
title: "Types of Software Documentation"
teaching: 7
exercises: 5

---

::::::::::::::::::::::::::::::::::::::: objectives

- Become familiar with the two main categories of software documentation and how they differ.
- Recognize the four modes of the Diátaxis framework.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What are the different types of software documentation?
- How do the types differ?
- How can the Diátaxis framework help organize documentation?

::::::::::::::::::::::::::::::::::::::::::::::::::

## The Types of Software Documentation

In our discussion of documentation, we will focus on two overarching
categories: _Developer_ and _User_.

![](fig/undraw-dev.png){alt='Undraw.co image of a developer'}
![](fig/undraw-user.png){alt='Undraw.co image of a user'}


### But wait... aren't there more?

You may be sitting there and asking this question. Many different sources will
list various alternative types of documentation such as requirements
documentation and testing documentation.

These specific sub-types of documentation can be categorized into the two
types listed here. We provide some examples below:

| Category | Examples |
| -------- | -------- |
| Developer | Requirements documentation; testing documentation; API documentation |
| User | How-to guides; tutorials; troubleshooting guidelines |

:::::::::::::::::::::::::::::::::::::::  challenge

## Can you think of more?

What other types of documentation can you think of? Do they fit into
the categories above?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Characteristics of Each Type

| Category | Intent | Target Audience |
| -------- | ------ | --------------- |
| Developer | Inform developers how to interface with a software package across the whole development lifecycle, including team processes. | Developers, technical stakeholders, team members |
| User | Help users succeed with a package from installation through everyday use, including examples and troubleshooting. | End-users, stakeholders |

## A Modern Take: The Diátaxis Framework

The developer/user split tells you *who* you're writing for. [Diátaxis](https://diataxis.fr/)
is a popular complementary framework that asks *what kind of help* the reader needs right now.
It identifies **four modes**:

| Mode | Serves | Answers... | Example |
|------|--------|----------|---------|
| **Tutorial** | Learning | "Teach me, step by step." | A guided first project |
| **How-to guide** | A task | "How do I accomplish X?" | "How to connect to the database" |
| **Reference** | Looking up | "What exactly does this do?" | API docs, config options |
| **Explanation** | Understanding | "Why does it work this way?" | A design-decisions write-up |

The key insight: these modes have **different goals and shouldn't be mixed**. A tutorial
clogged with reference detail stops teaching; reference docs padded with explanation get hard
to scan. Diátaxis maps neatly onto the categories above — tutorials and how-to guides lean
*user*, reference and explanation often serve *both* — so you can use both lenses together.

:::::::::::::::::::::::::::::::::::::::: keypoints

- There are two primary categories for documentation: developer and user.
- Developer documentation describes how developers should interface with a software package.
- User documentation helps users be more successful in using a software package.
- The Diátaxis framework adds a second lens — tutorials, how-to guides, reference, and explanation — and warns against mixing these modes.

::::::::::::::::::::::::::::::::::::::::::::::::::

