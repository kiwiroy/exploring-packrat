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
R 3.3.0; ; 2018-01-08 01:37:18 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:51:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:51:03 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:35:02 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:20 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:38:03 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:16 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:38 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:38:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:24 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:38:28 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:50:42 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:50:05 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:37:26 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:50:07 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:27 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:51:07 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:51:13 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:30 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:19 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:47:00 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:35 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:38:17 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:38 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:37:40 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:36:31 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:36:51 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:37:43 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:51:23 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:51:19 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:47:25 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; ; 2018-01-08 01:50:24 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:38:21 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:37:50 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2018-01-08 01:50:10 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
base
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Base Package
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:38:46 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
boot
</td>
<td style="text-align:left;">
1.3.18
</td>
<td style="text-align:left;">
Bootstrap Functions (Originally by Angelo Canty for S)
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:48:22 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:19 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
cluster
</td>
<td style="text-align:left;">
2.0.4
</td>
<td style="text-align:left;">
"Finding Groups in Data": Cluster Analysis Extended Rousseeuw et al.
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:48:39 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
codetools
</td>
<td style="text-align:left;">
0.2.14
</td>
<td style="text-align:left;">
Code Analysis Tools for R
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:48:50 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
compiler
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Compiler Package
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:32:54 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
datasets
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Datasets Package
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:37:00 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
foreign
</td>
<td style="text-align:left;">
0.8.66
</td>
<td style="text-align:left;">
Read Data Stored by Minitab, S, SAS, SPSS, Stata, Systat, Weka, dBase, ...
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:48:53 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
graphics
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Graphics Package
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:35:22 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
grDevices
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Graphics Devices and Support for Colours and Fonts
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:35:10 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
grid
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The Grid Graphics Package
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:38:20 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:02 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
lattice
</td>
<td style="text-align:left;">
0.20.33
</td>
<td style="text-align:left;">
Trellis Graphics for R
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:40:14 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
MASS
</td>
<td style="text-align:left;">
7.3.45
</td>
<td style="text-align:left;">
Support Functions and Datasets for Venables and Ripley's MASS
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:39:45 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
Matrix
</td>
<td style="text-align:left;">
1.2.6
</td>
<td style="text-align:left;">
Sparse and Dense Matrix Classes and Methods
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:40:56 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
methods
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Formal Methods and Classes
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:37:02 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
mgcv
</td>
<td style="text-align:left;">
1.8.12
</td>
<td style="text-align:left;">
Mixed GAM Computation Vehicle with GCV/AIC/REML Smoothness Estimation
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:33 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
nlme
</td>
<td style="text-align:left;">
3.1.127
</td>
<td style="text-align:left;">
Linear and Nonlinear Mixed Effects Models
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:46:10 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:22 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
parallel
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Support for Parallel computation in R
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:38:43 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
rpart
</td>
<td style="text-align:left;">
4.1.10
</td>
<td style="text-align:left;">
Recursive Partitioning and Regression Trees
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:08 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
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
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:49:27 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
splines
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Regression Spline Functions and Classes
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:38:34 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stats
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Stats Package
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:35:38 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
stats4
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Statistical Functions using S4 Classes
</td>
<td style="text-align:left;">
R 3.3.0; ; 2017-07-03 02:38:37 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
survival
</td>
<td style="text-align:left;">
2.39.2
</td>
<td style="text-align:left;">
Survival Analysis
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:47:10 UTC; unix
</td>
<td style="text-align:left;">
CRAN
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
tcltk
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Tcl/Tk Interface
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:38:40 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
tools
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
Tools for Package Development
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:32:53 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
<tr>
<td style="text-align:left;">
utils
</td>
<td style="text-align:left;">
3.3.0
</td>
<td style="text-align:left;">
The R Utils Package
</td>
<td style="text-align:left;">
R 3.3.0; x86\_64-pc-linux-gnu; 2017-07-03 02:34:43 UTC; unix
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
./packrat/lib-R/x86\_64-pc-linux-gnu/3.3.0
</td>
</tr>
</tbody>
</table>
