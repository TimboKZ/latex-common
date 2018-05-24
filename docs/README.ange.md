<%# output: ../README.md -%>
# latex-common

Useful LaTeX snippets and templates. This repository is a
[Rammy](https://github.com/TimboKZ/Rammy) module.

# Overview

Here you will find a brief overview of each snippet and template. Check the 
source code of each file for more info. To make it easier to preview templates,
compiled `.pdf`s have been included in the `templates/` folder.

<% const moduleConfig = require('../.rammyrc.json'); -%>

**Templates:**
<% for (const templateName in moduleConfig.templates) { -%>
<% const template = moduleConfig.templates[templateName]; -%>
* **<%- templateName %>** (`<%- template.path %>`) <%- template.description %>
<% } -%>

**Snippets:**
<% for (const snippetName in moduleConfig.snippets) { -%>
<% const snippet = moduleConfig.snippets[snippetName]; -%>
* **<%- snippetName %>** (`<%- snippet.path %>`) <%- snippet.description %>
<% } -%>

# Using with Rammy

If you have [Node.js](https://nodejs.org/) installed, you can use templates and
snippets in this repo via [Rammy](https://github.com/TimboKZ/Rammy).
Installation instructions:

```bash
# Install Rammy
npm install -g rammy

# Prepare a folder for the project, clone this repo into it
mkdir my-project
cd my-project

# Initialise a Rammy project, add this repo as a module
rammy init
rammy add TimboKZ/latex-common

# List templates and inputs Rammy discovered
rammy list

# Create TeX file for lecture notes using a template
rammy create notes.tex lectures-notes
```

# Using a Git submodule

It might be useful to at this repository as a Git submodule to your LaTeX
project. Run this command in the root folder of your project:

```bash
git submodule add https://github.com/TimboKZ/latex-common.git latex-common
```

You can now add files from the `snippets/` folder to your file using the
`\input{./path/to/snippet.tex}` command.
