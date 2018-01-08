Exploring `packrat`
================
Roy Storey
1/8/2018

Description
-----------

[packrat](http://rstudio.github.io/packrat/) is a package manager for R, much like pip for Python, cpanminus for perl, Bundler for Ruby gems, npm for node and yarn for javascript. Each of these package managers share a common goal of reproducibly installing an environment in which to run a user's code. Most allow for specification of the name and version of a list dependencies in a single file.

| manager   | language   | entity   | spec\_file         |
|:----------|:-----------|:---------|:-------------------|
| packrat   | R          | packages | `packrat.lock`     |
| pip       | Python     | modules  | `requirements.txt` |
| cpanminus | Perl       | modules  | `cpanfile`         |
| bundler   | Ruby       | gems     | `Gemfile`          |
| npm       | NodeJS     | packages | `package.json`     |
| yarn      | Javascript | packages | `package.json`     |

Usage
-----

Some of these steps are manual in other languages.

-   [walkthrough](http://rstudio.github.io/packrat/walkthrough.html)

### Initialisation

``` r
packrat::init()
```

### Installation

#### From an authored `packrat.lock`

``` r
packrat::restore()
```

#### While developing

``` r
install.packages(dplyr)
packrat::snapshot()
```
