# latex-common

Useful LaTeX snippets that can be added to a document using the `\input{../path/to.tex} ` command.

# Overview

You can find a brief overview of each file below. Consult the source code for more info.

* `symbols.tex` - common maths symbols (number sets, inner products, norms)
* `header.tex` - simple header for a file (header contents specified by defining `\HeaderTitle` command, e.g. `\newcommand\HeaderTitle{Problem set solutions}`).

# Using Git submodule

It might be useful to at this repository as a Git submodule to your LaTeX project. Run this command in the root folder of your project:

```bash
git submodule add https://github.com/TimboKZ/latex-common.git latex-common
```

