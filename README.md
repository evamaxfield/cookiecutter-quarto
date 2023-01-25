# Cookiecutter Quarto

[![Build Status](https://github.com/evamaxfield/cookiecutter-quarto/workflows/CI/badge.svg)](https://github.com/evamaxfield/cookiecutter-quarto/actions)

A cookiecutter to create a GitHub Repository that will build and render
[Quarto](https://quarto.org/) projects to `HTML`, `PDF`, and `DOCX` using
GitHub Actions and GitHub Pages.

## About

`Cookiecutter` is a Python package to generate templated projects.
This repository is a template for `cookiecutter` to generate a Quarto project which
contains following:

-   A directory structure for your project
-   Prebuilt `environment.yml` file to help you manage dependencies
    required for your project via
    [miniconda](https://docs.conda.io/en/latest/miniconda.html) environments.
-   Includes a [Justfile](https://github.com/casey/just) with basic commands
    to build, watch, and setup your project.
-   Continuous integration preconfigured to render the Quarto file (`index.qmd`):
    -   as a webpage and push to GitHub Pages
    -   as DOCX and PDF files which you can submit to a journal 

This cookiecutter is opinionated, feel free to fork this repository
and change it however you want.

## Quickstart

To use this template use the following commands.

1. `pip install cookiecutter`
2. `cookiecutter gh:evamaxfield/cookiecutter-quarto`

Once the project is generated, move to the newly created project directory
and follow the instructions in `README.md`.