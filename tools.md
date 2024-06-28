---
title: "Documentation Tools"
teaching: 10
exercises: 15
---

::::::::::::::::::::::::::::::::::::::: objectives

- "Become familiar with categories of tools to streamline documentation processes."
- "Practice using a small subset of documentation tools."

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- "What tools enable better documentation?"
- "What tools can streamline the documentation process?"

::::::::::::::::::::::::::::::::::::::::::::::::::

## Documentation Tools

There are plenty of tools to make documentation easier. In this episode,
we will cover just a few, but keep in mind, this is by no means an
exhaustive list.

### Style Guides and Standards

A good first step to streamline the documentation process is to create
or apply an existing style guide. This is useful both for developer
and user documentation.

For users, common standards and styles makes
the documentation predictable, consistent, and easier to read and use.
For developers, common standards and styles allow developers to focus more
on logic than styling and makes fewer ambiguities and increases the chance
that they will identify errors.

There is no single standard across all languages and projects. Some language
style guides have specific recommendations for in-line documentation like code comments and API documentation
(e.g., [Doxygen](https://www.doxygen.nl/), [Google](https://google.github.io/styleguide/),
[NumPy](https://numpydoc.readthedocs.io/en/latest/format.html#docstring-standard)).

:::::::::::::::::::::::::::::::::::::::  challenge

## PRACTICE: Google Style for Euler's Method

Google has many style guides, including a Python guide for
[writing docstrings](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings).

Using the Google style guide, write a docstring for the following class and its methods:

```python
class EulersMethod(self):
   def deriv(self, x, y):
       return y**2 + y*x + x**3
   def approx(self, y, x, h):
       y_j = y + h*self.deriv(x, y)
       x_j = x + h
       return y_j, x_j
```

::::::::::::::::::::::::::::::::::::::::::::::::::


### IDEs

Modern integrated development environments (IDEs) are applications that
combine text editing with other useful tools like building, testing, etc. Many
also enable automatic documentation generation in some variety. To name a few:

| IDE | Languages |
| --- | --------- |
| [VSCode](https://code.visualstudio.com/) |  PHP, HTML, CSS, SCSS, Less, JavaScript, JSON, TypeScript, Markdown, PowerShell, C++, Java, Python, Go, T-SQL, C#, .NET Core, etc. |
| [NetBeans](https://netbeans.apache.org/) | C, C++, C++11, Fortran, HTML 5, Java, PHP, etc. |
| [PyCharm](https://www.jetbrains.com/pycharm/) | AngularJS, Coffee Script, CSS, Cython, HTML, JavaScript, Node.js, Python, TypeScript |
| [Eclipse](https://www.eclipse.org/ide/) | C, C++, Java, Perl, PHP, Python, Ruby, etc. |

Many of these IDEs incorporate documentation generators that follow standard
style guides. For example, the [Spyder IDE](https://www.spyder-ide.org/) will
begin to generate docstrings based on your specified style guide.

![](fig/spyder-docstring.png){alt='Spyder IDE docstring settings'}

### Automated Generation

Another set of tools that streamline the documentation process are those that
automatically generate the documentation within your software package. The two
most popular documentation generators are:

1. [Doxygen](https://www.doxygen.nl/)
1. [Sphinx](https://www.sphinx-doc.org/en/master/)

Both of these tools will generate documentation, per configuration preferences,
and automatically integrate information like API documentation.

:::::::::::::::::::::::::::::::::::::::  challenge

## PRACTICE: Trying out Sphinx

We will quickly practice getting Sphinx set up on a project.

_NOTE_: These steps assume you are working from the command line and
have a clone of your practice repository.

0. (OPTIONAL, but recommended) Make a virtual Python environment
```bash
# MacOS/Linux
python -m venv virtual-python
source virtual-python/bin/activate
```
1. Install sphinx: `pip install sphinx`
2. Move to your practice directory: `cd /path/to/your/practice/repository`
3. Make and move to a document directory: `mkdir docs && cd docs`
4. Run Sphinx's quickstart: `sphinx-quickstart`
   (_NOTE_: Use default options as applicable; fill out everything else as you desire.)
5. Generate the documentation: `make html`
6. View your documentation: `open _build/html/index.html`

::::::::::::::::::::::::::::::::::::::::::::::::::

### Automated Publishing

Potentially the most helpful method of streamlining the documentation process
is to implement automated publishing. By implementing this, when a new feature
or change is merged into your code base, your documentation will be generated
and published automatically. Two popular documentation hosting tools are:

1. [ReadtheDocs](https://readthedocs.org/)
1. [GitHub Pages](https://pages.github.com/)

Both of these services will publish documentation from open source software
for free. They can be set up to publish the most recent version of all
documentation as soon as a new change is introduced to the main code.

We will practice doing this with GitHub Pages. Before getting into the
exercise, you will need to make sure GitHub Pages is activated on your
practice repository.

1. _Make a `gh-pages` branch_.
   Either from the GUI or through command line, make a new branch named `gh-pages`.
   In the GUI, you would do this by clicking on the branches link:
   ![](fig/branches.png){alt='GitHub Branches button highlighted'}
   Then click on "New branch":
   ![](fig/new-branch.png){alt='GitHub Branches new branch'}
   Name it `gh-pages`:
   ![](fig/gh-pages-branch.png){alt='GitHub Branches gh-pages branch'}
2. _Set up GitHub to build from that branch_.
   In the GUI, go to "Settings" > "Pages":
   ![](fig/gh-pages-setting.png){alt='GitHub Pages Settings'}
   Change the settings to "Source: Deploy from branch", "Branch: gh-pages", and
   "directory /docs". Then hit "Save."
   ![](fig/gh-pages-final-settings.png){alt='GitHub Pages final settings'}

Now complete the following exercise!

:::::::::::::::::::::::::::::::::::::::  challenge

## PRACTICE: Sphinx to GitHub Pages

Now that we have some starter documentation, let's publish it to
GitHub Pages.

_NOTE_: These steps assume you are working from the command line and
have a clone of your practice repository.

1. Make a local copy of the `gh-pages` branch: `git -b checkout gh-pages`
2. Set your local copy to track GitHub's copy: `git push --set-upstream origin gh-pages`
3. Move to the `docs` directory and clean up the previous build: `cd docs && make clean`
4. Change the default build location: For `Makefile` and `make.bat`, change `BUILDDIR = _build` to `BUILDDIR = .`
5. Make your documentation: `make html`
6. Make a file `index.html` in the `docs` directory with the content:
  `<meta http-equiv="refresh" content="0; url=./html/index.html" />` (_NOTE_: This tells GitHub to use the `html/index.html` file as the main page.)
7. Add all your changes, commit, and push: `git add docs/ && git commit -m "Add documentation to GitHub Pages" && git push`
8. Wait a minute or two, then view your documentation at https://YOURUSERNAME.github.io/intersect-practice-repo/html/index.html

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::  callout

## What happened to the styling?!

GitHub renders styles in a unique way using [Jekyll](https://jekyllrb.com/). We can turn this
off by adding an empty `.nojekyll` file in the `docs` directory.

:::::::::::::::::::::::::::::::::::::::::::::::::::

That's it! You now know some useful tips and tricks for making better documentation.

:::::::::::::::::::::::::::::::::::::::: keypoints

- "Documentation tools vary from styles to text editors to automation."
- "Many tools have quick-start capabilities to get small or new projects started with better documentation processes."

::::::::::::::::::::::::::::::::::::::::::::::::::

