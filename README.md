# latex-common

Useful LaTeX snippets that can be added to a document using the `\input{../path/to.tex} ` command.

# Overview

You can find a brief overview of each file below. Consult the source code for more info.

* `symbols.tex` - common maths symbols (number sets, inner products, norms)
* `header.tex` - simple header for a file (header contents specified by defining `\HeaderTitle` command, e.g. `\newcommand\HeaderTitle{Problem set solutions}`).

# Using a Git submodule

It might be useful to at this repository as a Git submodule to your LaTeX
project. Run this command in the root folder of your project:

```bash
git submodule add https://github.com/TimboKZ/latex-common.git latex-common
```

# Using Rammy

If you have [Node.js](https://nodejs.org/) installed, you can use templates and
snippets in this repo via Rammy. Installation instructions:

```bash
# Install Rammy
npm install -g rammy

# Prepare a folder for the project, clone this repo into it
mkdir my-project
cd my-project
git clone https://github.com/TimboKZ/latex-common.git

# Initialise a Rammy project, add this repo as a module
rammy init
rammy add ./latex-common

# List templates and inputs Rammy discovered
rammy list

# Create TeX file for lecture notes using a template
rammy create notes.tex lectures-notes
```

