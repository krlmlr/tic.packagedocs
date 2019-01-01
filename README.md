# tic.packagedocs

[![Travis-CI Build Status](https://travis-ci.org/krlmlr/tic.packagedocs.svg?branch=master)](https://travis-ci.org/krlmlr/tic.packagedocs) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/krlmlr/tic.packagedocs?branch=master&svg=true)](https://ci.appveyor.com/project/krlmlr/tic.packagedocs) [![Coverage Status](https://codecov.io/gh/krlmlr/tic.packagedocs/branch/master/graph/badge.svg)](https://codecov.io/github/krlmlr/tic.packagedocs?branch=master)

A minimal example package with [packagedocs](http://hafen.github.io/packagedocs) documentation created and uploaded by _tic_.
The documentation is written to, and served from, the `gh-pages` branch.
_tic_ is an R package for CI-agnostic workflow definitions for various R projects. 
See its [documentation](https://ropenscilabs.github.io/tic/) for more information.

## Comparing to a conventional setup

Only a few files are added or changed to enable integration with _tic_:

- [`tic.R`](blob/master/tic.R): This file describes the CI workflow.
- [`.travis.yml`](blob/master/.travis.yml): This file translates between CI stages of Travis CI and _tic_ stages.
- [`appveyor.yml`](blob/master/appveyor.yml): This file translates between CI stages of AppVeyor and _tic_ stages.
- [`.Rbuildignore`](blob/master/.Rbuildignore): The files listed above are not part of a built R package and must be excluded.

## Set up an operational fork of this repository

If you want to experiment with _travis_ and _tic_ in this repo, you can fork it.

1. Use `usethis::create_from_github()` to automatically create a fork of this repo.
    If you use RStudio, a new RStudio project will open. 
    You may need to set up your SSH credentials first. See [this guide](http://happygitwithr.com/ssh-keys.html) if you're having problems. 
    (It's definitely worth getting this function running as it saves you so much time in the future!) 
    Alternatively, fork this repo on Github and then create a new R Project within RStudio (File -> New Project -> Version Control -> Github). 
1. Run `travis::use_tic()` to set up all requirements needed for the CI integration of your package.