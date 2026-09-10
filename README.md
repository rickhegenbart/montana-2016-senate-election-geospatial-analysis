# Geospatial and Demographic Patterns in the 2016 Montana U.S. Senate Election

> **Master’s Psychology Research & Analytics Portfolio**
>
> This project was completed as part of my Master’s degree program in Psychology. It applies R-based data analysis, geospatial visualization, and regression to examine county-level voting patterns in Montana’s 2016 U.S. Senate election.
>
> [View the complete Master’s Psychology Research & Analytics Portfolio](https://github.com/users/rickhegenbart/projects/1)

## Overview

This project combines county-level election results with American Community Survey population data and geographic boundaries to examine patterns in the 2016 Montana U.S. Senate election.

The analysis calculates Republican vote advantage by county, maps geographic variation, and examines associations between vote advantage, county population, and longitude.

This is a nonpartisan academic analysis of historical election data. It describes observed relationships and does not make causal claims or political recommendations.

## Analysis Questions

* How did Republican vote advantage vary across Montana counties?
* What geographic patterns were visible in county-level vote advantage?
* What association was observed between county population and Republican vote advantage?
* What association was observed between longitude and Republican vote advantage?
* How did population and longitude relate jointly to county-level vote advantage?

## Methods

The analysis:

* Imports county-level 2016 Montana Senate-election results.
* Calculates total votes and Republican vote advantage.
* Retrieves county population estimates and geographic boundaries through the U.S. Census API.
* Merges election, population, and geographic data.
* Creates interactive county maps with `leaflet`.
* Produces interactive scatterplots with `plotly`.
* Fits linear-regression models examining associations with population and longitude.

## Tools

* R
* R Markdown
* `tidyverse`
* `leaflet`
* `sf`
* `readxl`
* `DT`
* `plotly`
* `broom`
* `tidycensus`

## Data and Security

The original analysis uses:

```text
Statewide Results.xlsx
```

It also retrieves American Community Survey data through the U.S. Census API.

The election-results workbook is not currently included in this repository. Document its original source and redistribution permissions before adding it.

Do not commit API keys, `.Renviron` files, or other credentials. Store your Census API key locally in a `.Renviron` file:

```text
CENSUS_API_KEY=your_key_here
```

## Repository Contents

```text
├── README.md
└── MT_2016_Senate_Election(20260910-201957).Rmd
```

## Reproducing the Analysis

Install the required R packages:

```r
install.packages(c(
  "tidyverse", "leaflet", "sf", "readxl",
  "DT", "plotly", "broom", "tidycensus"
))
```

Add a permitted `Statewide Results.xlsx` file, configure your Census API key locally, and then render the R Markdown file.

## Project Status

This repository preserves the original geospatial analysis source code. A reproducible HTML report can be added after the election-results workbook and source documentation are available.
