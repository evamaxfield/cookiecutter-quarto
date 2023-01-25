# {{ cookiecutter.project_name }}

[![CI](https://github.com/{{ cookiecutter.hosting_github_username_or_org }}/{{ cookiecutter.project_slug }}/actions/workflows/ci.yml/badge.svg)](https://github.com/{{ cookiecutter.hosting_github_username_or_org }}/{{ cookiecutter.project_slug }}/actions/workflows/ci.yml)

This repository stores the files needed for [Quarto](https://quarto.org/)
to generate our paper "{{ cookiecutter.project_name }}".

View the rendered article at: [https://{{ cookiecutter.hosting_github_username_or_org }}.github.io/{{ cookiecutter.project_slug }}/](https://{{ cookiecutter.hosting_github_username_or_org }}.github.io/{{ cookiecutter.project_slug }}/)

## Abstract

TODO: Fill in your abstract so it makes it easier to search on GitHub as well.

---

## Setup

1.  Install [Quarto](https://quarto.org/docs/get-started/).
2.  Install [Just](https://github.com/casey/just#packages).
3.  Run `just setup` to create a new conda environment with all dependencies.
4.  Run `conda activate councils-in-action` to activate the environment.
5.  Build!
    - `just build` to build the project to the `_build/` folder.
    - `just watch` to watch this directory and build just the website on file save.

You may run into issues running your first `just build` command. If the issue relates to
`tinytex` or `texlive` then try installing the latest versions:

* Install:
`sudo apt-get install texlive-xetex texlive-fonts-recommended texlive-plain-generic`
* Or Upgrade:
`sudo apt-get upgrade texlive-xetex texlive-fonts-recommended texlive-plain-generic`

### File Structure

```
├── environment.yml # Conda environment.yml file for project dependencies
├── index.qmd       # Quarto file where you should place your content
├── Justfile        # Command runner
├── _quarto.yml     # General Quarto settings file
├── README.md       # This file!
└── support         # Directory for figures, bibtex and CSL files
    ├── figs        # Directory for figures
    ├── main.bib    # bibtex file for citations
    └── pnas.csl    # Citation Style Language file
```

### Development Commands

```
just --list
Available recipes:
    build   # build page
    clean   # remove build files
    default # list all available commands
    setup name="councils-in-action" # create conda env and install all deps
    watch   # watch file, build, and serve
```

### GitHub Setup

1.  Turn your project into a GitHub repository:
    -   Make an account on [github.com](https://github.com)
    -   Go to [make a new repository](https://github.com/new)
    -   Set the repository name to '{{ cookiecutter.project_slug }}'
    -   After a GitHub repo has been created, push your files to
        the new repo following GitHub's instructions.
2.  After the first successful GitHub Action completes,
    ensure that you have set GitHub pages to build the `gh-pages` branch by selecting the
    `gh-pages` branch in the dropdown in the "GitHub Pages" section of the
    repository settings.
    ([Repo Settings](https://github.com/{{ cookiecutter.hosting_github_username_or_org }}/{{ cookiecutter.project_slug }}/settings))

