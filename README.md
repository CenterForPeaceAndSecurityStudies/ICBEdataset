
<!-- README.md is generated from README.Rmd. Please edit that file -->
## The International Crisis Behavior Events (ICBe)

This is a github repository for the International Crisis Behavior Events (ICBe) dataset. Submit any issues regarding the dataset, paper, or github repository using [the issues tab](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/issues/new/choose).

# The Paper:

[Introducing the International Crisis Behavior Event (ICBe) Dataset](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/paper/IntroducingICBe_DouglassEtAl_2021_BetaDraft_bookdown.pdf)

## The Authors:

-   [Rex W. Douglass](http://www.rexdouglass.com), [Thomas Leo Scherer](http://tlscherer.com/), [J. Andrés Gannon](https://jandresgannon.com/), [Erik Gartzke](http://erikgartzke.com/), [Jon Lindsay](https://www.jonrlindsay.com/), [Shannon Carcelli](https://www.shannoncarcelli.com/), Jonathan Wilkenfeld, David M. Quinn, Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle Murauskaite, and Diana Partridge.

## Data:

# ICBe Dataset

-   ICBe Dataset
-   [ICBEdataset Codebook](https://docs.google.com/document/d/1aJkweohbfIWtNpJw1CmXbeIiK6czbJ5iPyKwiYP1YlU/edit?usp=sharing)

## Replication Code and Analysis

### Self Contained Package

All of the files necessary for reproducing our analysis are including in a self contained R package "ICBEdataset" You can install the package icb from github with:

``` r
# install.packages("devtools")
devtools::install_github("centerforpeaceandsecuritystudies/ICBEdataset")
```

## RMarkdown files

-   01\_compile\_saves\_and\_align
    -   compiles the original coding files into `./replication_data/temp/icb_coder_crisis_sentence_event.Rds`
    -   the original coding files are not on the public repository; this can only be run by authors
    -   aligns codings from multiple GUI versions on similar source sentences
    -   creates `./data/icb_code_crisis_sentence_event_aligned.Rds`
-   02\_format\_and\_clean
    -   applies cleaning dictionaries to create `./data/icb_wide_clean.Rds` and `./data/icb_long_clean.Rds`.
-   03\_aggregation
    -   applies aggregation algorithm to create `./data_out/codings_long.Rds`, `./data_out/codings_long_agreement.Rds`, `./data_out/codings_long_agreed.Rds`, `./data_out/codings_wide_agreed.Rds`.

## ICBe raw data

-   Agreed Data, long form (LINK NEEDED)
-   Agreed Data, wide form (LINK NEEDED)
-   [Clean data, wide form](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/data/icb_wide_clean.Rds)
    -   each row is a coder-crisis-event-sentence (i.e. each time a coder looking at a certain sentence in a certain crisis identified an event)
    -   values may contain multiple entries separating with a semicolon
-   [Clean data, long form](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/data/icb_long_clean.Rds)
    -   each row contains identifying information for a coder-crisis-event-sentence
    -   the information about that sentence is distributed across multiple rows in the columns *variable* and *value*
    -   each value contains a single entry
-   [Raw codings](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/data/icb_coder_crisis_sentence_event_aligned.Rds)
    -   the initial codings from different GUI versions adjusted so that sentence numbers are aligned.

## Other data inputs:

### ICBe prep

-   Cleaning dictionaries: used to clean raw codings for actors, actions, locations, and dates [available online](https://docs.google.com/spreadsheets/d/1a7Id0Zg41PTKEv74H_KjiJzhMak2jGh0leT7B8oVWdI/edit#gid=0) and ./data/icb\_manual\_recording\_master\_sheet.xlsx
-   actor\_translator to compare actors across different datasets, created by hand with assistance from [07\_actor\_dictionaries](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/07_actor_dictionaries.html).
-   [Lit review and tree/leaf codebook](https://docs.google.com/spreadsheets/d/10tZGzjYgmvrbgQTV3oadVEV8m1LxLEDJEq9pzqq90Fc/edit#gid=1604363724)

### Existing datasets

-   [The ICB project](https://sites.duke.edu/icbdata/) system-level (./data/icb1v14.Rds) and actor-level (./data/icb2v14.Rds) datasets.
-   [ICEWS data sample](https://dataverse.harvard.edu/file.xhtml?persistentId=doi:10.7910/DVN/28075/WNOBVV&version=30.0) from 1995 (./inst/extdata/icews.actors.20181119.RData).

### Acknowledgementes
