
<!-- README.md is generated from README.Rmd. Please edit that file -->
## The International Crisis Behavior Events (ICBe)

This is a github repository for the International Crisis Behavior Events (ICBe) dataset. Submit any issues regarding the dataset, paper, or github repository using [the issues tab](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/issues/new/choose).

# The Paper:

[Introducing the International Crisis Behavior Event (ICBe) Dataset](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/paper/IntroducingICBe_DouglassEtAl_2021_BetaDraft_bookdown.pdf)

## The Authors:

-   [Rex W. Douglass](http://www.rexdouglass.com), [Thomas Leo Scherer](http://tlscherer.com/), [J. Andrés Gannon](https://jandresgannon.com/), [Erik Gartzke](http://erikgartzke.com/), [Jon Lindsay](https://www.jonrlindsay.com/), [Shannon Carcelli](https://www.shannoncarcelli.com/), Jonathan Wilkenfeld, David M. Quinn, Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle Murauskaite, and Diana Partridge.

# ICBe Dataset

-   ICBe Dataset
-   [ICBEdataset Codebook](https://docs.google.com/document/d/1aJkweohbfIWtNpJw1CmXbeIiK6czbJ5iPyKwiYP1YlU/edit?usp=sharing)

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

## Replication Code and Analysis

### Self Contained Package

All of the files necessary for reproducing our analysis are including in a self contained R package "ICBEdataset" You can install the package icb from github with:

``` r
# install.packages("devtools")
devtools::install_github("centerforpeaceandsecuritystudies/ICBEdataset")
```

## RMarkdown files

-   [01\_compile\_saves](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/01_compile_saves.html)
    -   compiles the original coding files into `./data/icb_coder_crisis_sentence_event.tsv`
    -   the original coding files are not on the public repository; this can only be run by authors
-   [02\_align\_sentences](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/02_align_sentences.html)
    -   aligns codings from multiple GUI versions on similar source sentences
    -   creates `./data/icb_code_crisis_sentence_event_aligned.Rds`
-   [03\_format\_and\_clean](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/03_format_and_clean.html)
    -   applies cleaning dictionaries to create `./data/icb_wide_clean.Rds` and `./data/icb_long_clean.Rds`.
-   [04\_aggregation](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/04_aggregation.html)
    -   applies aggregation algorithm to create `./data_out/codings_long.Rds`, `./data_out/codings_long_agreement.Rds`, `./data_out/codings_long_agreed.Rds`, `./data_out/codings_wide_agreed.Rds`.
-   [05a\_data\_summary](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/05a_data_summary.html)
    -   coding information, sentence root, time, coder confidence
-   [05b\_data\_summary](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/05b_data_summary.html)
    -   actions, speech, thought

## Other data inputs:

### ICBe prep

-   Cleaning dictionaries: used to clean raw codings for actors, actions, locations, and dates [available online](https://docs.google.com/spreadsheets/d/1a7Id0Zg41PTKEv74H_KjiJzhMak2jGh0leT7B8oVWdI/edit#gid=0) and ./data/icb\_manual\_recording\_master\_sheet.xlsx
-   actor\_translator to compare actors across different datasets, created by hand with assistance from [07\_actor\_dictionaries](https://centerforpeaceandsecuritystudies.github.io/ICBEdataset/07_actor_dictionaries.html).
-   [Lit review and tree/leaf codebook](https://docs.google.com/spreadsheets/d/10tZGzjYgmvrbgQTV3oadVEV8m1LxLEDJEq9pzqq90Fc/edit#gid=1604363724)

### Existing datasets

-   [The ICB project](https://sites.duke.edu/icbdata/) system-level (./data/icb1v14.Rds) and actor-level (./data/icb2v14.Rds) datasets.
-   [ICEWS data sample](https://dataverse.harvard.edu/file.xhtml?persistentId=doi:10.7910/DVN/28075/WNOBVV&version=30.0) from 1995 (./inst/extdata/icews.actors.20181119.RData).

### Acknowledgementes
