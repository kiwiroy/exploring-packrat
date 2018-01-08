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

### State

``` r
packrat::status()
```

#### Save

``` r
packrat::snapshot()
```

### What is installed?

<table>
<thead>
<tr>
<th style="text-align:left;">
Package
</th>
<th style="text-align:left;">
Version
</th>
<th style="text-align:left;">
Title
</th>
<th style="text-align:left;">
Built
</th>
<th style="text-align:left;">
Repo
</th>
<th style="text-align:left;">
LibPath
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
assertthat
</td>
<td style="text-align:left;">
0.2.0
</td>
<td style="text-align:left;">
Easy Pre and Post Assertions
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 21:17:22 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
backports
</td>
<td style="text-align:left;">
1.1.2
</td>
<td style="text-align:left;">
Reimplementations of Functions Introduced Since R-3.0.0
</td>
<td style="text-align:left;">
R 3.4.3; x86\_64-apple-darwin15.6.0; 2017-12-14 08:46:34 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
base64enc
</td>
<td style="text-align:left;">
0.1.3
</td>
<td style="text-align:left;">
Tools for base64 encoding
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 21:26:37 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
BH
</td>
<td style="text-align:left;">
1.65.0.1
</td>
<td style="text-align:left;">
Boost C++ Header Files
</td>
<td style="text-align:left;">
R 3.4.1; ; 2017-08-25 04:28:47 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
bindr
</td>
<td style="text-align:left;">
0.1
</td>
<td style="text-align:left;">
Parametrized Active Bindings
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-22 01:29:35 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
bindrcpp
</td>
<td style="text-align:left;">
0.2
</td>
<td style="text-align:left;">
An 'Rcpp' Interface to Active Bindings
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-06-18 06:32:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
bitops
</td>
<td style="text-align:left;">
1.0.6
</td>
<td style="text-align:left;">
Bitwise Operations
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 21:59:50 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
caTools
</td>
<td style="text-align:left;">
1.17.1
</td>
<td style="text-align:left;">
Tools: moving window statistics, GIF, Base64, ROC AUC, etc.
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 22:12:36 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
cli
</td>
<td style="text-align:left;">
1.0.0
</td>
<td style="text-align:left;">
Helpers for Developing Command Line Interfaces
</td>
<td style="text-align:left;">
R 3.4.2; ; 2017-11-06 09:28:23 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
crayon
</td>
<td style="text-align:left;">
1.3.4
</td>
<td style="text-align:left;">
Colored Terminal Output
</td>
<td style="text-align:left;">
R 3.4.1; ; 2017-09-17 04:43:27 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
digest
</td>
<td style="text-align:left;">
0.6.13
</td>
<td style="text-align:left;">
Create Compact Hash Digests of R Objects
</td>
<td style="text-align:left;">
R 3.4.3; x86\_64-apple-darwin15.6.0; 2017-12-15 05:21:16 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
dplyr
</td>
<td style="text-align:left;">
0.7.4
</td>
<td style="text-align:left;">
A Grammar of Data Manipulation
</td>
<td style="text-align:left;">
R 3.4.2; x86\_64-apple-darwin15.6.0; 2017-09-29 04:33:12 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
evaluate
</td>
<td style="text-align:left;">
0.10.1
</td>
<td style="text-align:left;">
Parsing and Evaluation Tools that Provide More Details than the Default
</td>
<td style="text-align:left;">
R 3.4.1; ; 2017-07-03 11:17:49 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
formatR
</td>
<td style="text-align:left;">
1.5
</td>
<td style="text-align:left;">
Format R Code Automatically
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-26 03:41:45 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
glue
</td>
<td style="text-align:left;">
1.2.0
</td>
<td style="text-align:left;">
Interpreted String Literals
</td>
<td style="text-align:left;">
R 3.4.2; x86\_64-apple-darwin15.6.0; 2017-10-30 08:48:16 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
highr
</td>
<td style="text-align:left;">
0.6
</td>
<td style="text-align:left;">
Syntax Highlighting for R Source Code
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 21:21:08 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
htmltools
</td>
<td style="text-align:left;">
0.3.6
</td>
<td style="text-align:left;">
Tools for HTML
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-29 03:24:16 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
jsonlite
</td>
<td style="text-align:left;">
1.5
</td>
<td style="text-align:left;">
A Robust, High Performance JSON Parser and Generator for R
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-06-02 03:53:14 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
knitr
</td>
<td style="text-align:left;">
1.18
</td>
<td style="text-align:left;">
A General-Purpose Package for Dynamic Report Generation in R
</td>
<td style="text-align:left;">
R 3.4.3; ; 2017-12-28 05:42:36 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
magrittr
</td>
<td style="text-align:left;">
1.5
</td>
<td style="text-align:left;">
A Forward-Pipe Operator for R
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 21:17:20 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
markdown
</td>
<td style="text-align:left;">
0.8
</td>
<td style="text-align:left;">
'Markdown' Rendering for R
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 21:21:20 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
mime
</td>
<td style="text-align:left;">
0.5
</td>
<td style="text-align:left;">
Map Filenames to MIME Types
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 21:12:03 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
packrat
</td>
<td style="text-align:left;">
0.4.8.54
</td>
<td style="text-align:left;">
A Dependency Management System for Projects and their R Package Dependencies
</td>
<td style="text-align:left;">
R 3.4.0; ; 2018-01-08 23:25:04 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
pillar
</td>
<td style="text-align:left;">
1.0.1
</td>
<td style="text-align:left;">
Coloured Formatting for Columns
</td>
<td style="text-align:left;">
R 3.4.3; ; 2017-11-28 05:21:28 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
pkgconfig
</td>
<td style="text-align:left;">
2.0.1
</td>
<td style="text-align:left;">
Private Configuration for 'R' Packages
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-20 18:51:07 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
plogr
</td>
<td style="text-align:left;">
0.1.1
</td>
<td style="text-align:left;">
The 'plog' C++ Logging Library
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 21:51:53 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
R6
</td>
<td style="text-align:left;">
2.2.2
</td>
<td style="text-align:left;">
Classes with Reference Semantics
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-06-18 04:09:19 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
Rcpp
</td>
<td style="text-align:left;">
0.12.14
</td>
<td style="text-align:left;">
Seamless R and C++ Integration
</td>
<td style="text-align:left;">
R 3.4.3; x86\_64-apple-darwin15.6.0; 2017-11-24 05:22:56 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
rlang
</td>
<td style="text-align:left;">
0.1.6
</td>
<td style="text-align:left;">
Functions for Base Types and Core R and 'Tidyverse' Features
</td>
<td style="text-align:left;">
R 3.4.3; x86\_64-apple-darwin15.6.0; 2017-12-22 05:23:43 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
rmarkdown
</td>
<td style="text-align:left;">
1.8
</td>
<td style="text-align:left;">
Dynamic Documents for R
</td>
<td style="text-align:left;">
R 3.4.2; ; 2017-11-18 05:50:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
rprojroot
</td>
<td style="text-align:left;">
1.3.2
</td>
<td style="text-align:left;">
Finding Files in Project Subdirectories
</td>
<td style="text-align:left;">
R 3.4.0; ; 2018-01-08 23:32:01 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stringi
</td>
<td style="text-align:left;">
1.1.6
</td>
<td style="text-align:left;">
Character String Processing Facilities
</td>
<td style="text-align:left;">
R 3.4.2; x86\_64-apple-darwin15.6.0; 2017-11-18 05:56:42 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stringr
</td>
<td style="text-align:left;">
1.2.0
</td>
<td style="text-align:left;">
Simple, Consistent Wrappers for Common String Operations
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-20 17:42:13 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
tibble
</td>
<td style="text-align:left;">
1.4.1
</td>
<td style="text-align:left;">
Simple Data Frames
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2018-01-08 23:32:11 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
utf8
</td>
<td style="text-align:left;">
1.1.3
</td>
<td style="text-align:left;">
Unicode Text Processing
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2018-01-08 23:31:55 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
yaml
</td>
<td style="text-align:left;">
2.1.16
</td>
<td style="text-align:left;">
Methods to Convert R Data to YAML and Back
</td>
<td style="text-align:left;">
R 3.4.3; x86\_64-apple-darwin15.6.0; 2017-12-13 05:37:43 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
base
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Base Package
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:29:28 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
boot
</td>
<td style="text-align:left;">
1.3.19
</td>
<td style="text-align:left;">
Bootstrap Functions (Originally by Angelo Canty for S)
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:35:29 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
class
</td>
<td style="text-align:left;">
7.3.14
</td>
<td style="text-align:left;">
Functions for Classification
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:32:14 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
cluster
</td>
<td style="text-align:left;">
2.0.6
</td>
<td style="text-align:left;">
"Finding Groups in Data": Cluster Analysis Extended Rousseeuw et al.
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:32:14 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
codetools
</td>
<td style="text-align:left;">
0.2.15
</td>
<td style="text-align:left;">
Code Analysis Tools for R
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:31:32 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
compiler
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Compiler Package
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:23:34 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
datasets
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Datasets Package
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:27:59 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
foreign
</td>
<td style="text-align:left;">
0.8.67
</td>
<td style="text-align:left;">
Read Data Stored by Minitab, S, SAS, SPSS, Stata, Systat, Weka, dBase, ...
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:33 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
graphics
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Graphics Package
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:26:44 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
grDevices
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Graphics Devices and Support for Colours and Fonts
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:25:51 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
grid
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The Grid Graphics Package
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:28:52 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
KernSmooth
</td>
<td style="text-align:left;">
2.23.15
</td>
<td style="text-align:left;">
Functions for Kernel Smoothing Supporting Wand & Jones (1995)
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:33 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
lattice
</td>
<td style="text-align:left;">
0.20.35
</td>
<td style="text-align:left;">
Trellis Graphics for R
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:34 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
MASS
</td>
<td style="text-align:left;">
7.3.47
</td>
<td style="text-align:left;">
Support Functions and Datasets for Venables and Ripley's MASS
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:36 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
Matrix
</td>
<td style="text-align:left;">
1.2.9
</td>
<td style="text-align:left;">
Sparse and Dense Matrix Classes and Methods
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:32:11 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
methods
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Formal Methods and Classes
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:28:07 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
mgcv
</td>
<td style="text-align:left;">
1.8.17
</td>
<td style="text-align:left;">
Mixed GAM Computation Vehicle with GCV/AIC/REML Smoothness Estimation
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:34:28 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
nlme
</td>
<td style="text-align:left;">
3.1.131
</td>
<td style="text-align:left;">
Linear and Nonlinear Mixed Effects Models
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:32:10 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
nnet
</td>
<td style="text-align:left;">
7.3.12
</td>
<td style="text-align:left;">
Feed-Forward Neural Networks and Multinomial Log-Linear Models
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:33 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
parallel
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Support for Parallel computation in R
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:29:23 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
rpart
</td>
<td style="text-align:left;">
4.1.11
</td>
<td style="text-align:left;">
Recursive Partitioning and Regression Trees
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:35 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
spatial
</td>
<td style="text-align:left;">
7.3.11
</td>
<td style="text-align:left;">
Functions for Kriging and Point Pattern Analysis
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:31:33 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
splines
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Regression Spline Functions and Classes
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:29:10 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stats
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Stats Package
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:26:55 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stats4
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Statistical Functions using S4 Classes
</td>
<td style="text-align:left;">
R 3.4.0; ; 2017-04-21 20:29:14 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
survival
</td>
<td style="text-align:left;">
2.41.3
</td>
<td style="text-align:left;">
Survival Analysis
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:34:31 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
tcltk
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Tcl/Tk Interface
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:29:16 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
tools
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
Tools for Package Development
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:23:32 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
<tr>
<td style="text-align:left;">
utils
</td>
<td style="text-align:left;">
3.4.0
</td>
<td style="text-align:left;">
The R Utils Package
</td>
<td style="text-align:left;">
R 3.4.0; x86\_64-apple-darwin15.6.0; 2017-04-21 20:25:12 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-apple-darwin15.6.0/3.4.0
</td>
</tr>
</tbody>
</table>
Loading `.Rprofile`
-------------------

packrat uses `.Rprofile` in the current directory, the caveats for this are mentioned in the [documentation]().

``` r
## honour user .Rprofile
if (file.exists(Sys.getenv("R_PROFILE_USER"))) {
  source(Sys.getenv("R_PROFILE_USER"))
} else if(file.exists(path.expand("~/.Rprofile"))) {
  source(path.expand("~/.Rprofile"))
}
```

``` r
#### -- Packrat Autoloader (version 0.4.8-54) -- ####
source("packrat/init.R")
#### -- End Packrat Autoloader -- ####
```

packrat unloads any packages that `~/.Rprofile` loads so YMMV.

Source vs Binary
----------------

Version 0.4.9 fixes a [mirror build issue](https://github.com/rstudio/packrat/blame/master/NEWS.md#L20-L22) where a binary version of a release has not be built. This can manifest in a portability issue between a machine where source installs are the default and transitioning to a machine where binary installs are the default. i.e. Linux -&gt; macos

While 0.4.9 remains unreleased the options are

    1. bootstrapping must be performed outside a packrat project
        1.1 `install.packages('devtools')`
        1.2 `devtools::install_github('rstudio/packrat')`
    2. include packrat in `packrat/src` - possibly a good idea anyway @ 125KB overhead
        2.1 See [include-packrat branch](https://github.com/kiwiroy/exploring-packrat/tree/include-packrat)
