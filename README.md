
-   <a href="#the-international-crisis-behavior-events-icbe"
    id="toc-the-international-crisis-behavior-events-icbe">The International
    Crisis Behavior Events (ICBe)</a>
-   <a href="#the-paper" id="toc-the-paper">The Paper:</a>
-   <a href="#the-data" id="toc-the-data">The Data:</a>
-   <a href="#the-authors" id="toc-the-authors">The Authors:</a>
-   <a href="#citation" id="toc-citation">Citation:</a>
-   <a href="#replication-code-and-analysis"
    id="toc-replication-code-and-analysis">Replication Code and Analysis</a>
-   <a href="#data-preparation" id="toc-data-preparation">data
    preparation</a>
    -   <a href="#replication_corpus"
        id="toc-replication_corpus">replication_corpus</a>
    -   <a href="#replication_data"
        id="toc-replication_data">replication_data</a>
    -   <a href="#replication_paper"
        id="toc-replication_paper">replication_paper</a>
-   <a href="#data-inputs" id="toc-data-inputs">Data inputs:</a>
    -   <a href="#icbe-preparation" id="toc-icbe-preparation">ICBe
        preparation</a>
    -   <a href="#external-datasets" id="toc-external-datasets">External
        datasets</a>
    -   <a href="#appendix" id="toc-appendix">Appendix</a>
    -   <a href="#license-and-doi" id="toc-license-and-doi">License and DOI</a>

<!-- README.md is generated from README.Rmd. Please edit that file -->

[![CC BY-NC-SA
4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

## The International Crisis Behavior Events (ICBe)

This is a github repository for the International Crisis Behavior Events
(ICBe) dataset. Submit any issues regarding the dataset, paper, or
github repository using [the issues
tab](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/issues/new/choose).

## The Paper:

[Introducing the ICBe Dataset: Very High Recall and Precision Event
Extraction from Narratives about International
Crises](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/replication_paper/arxiv_draft/paper.pdf)
(also available on [ArXiv](https://arxiv.org/abs/2202.07081)).

The v1.1 Online Appendix can be downloaded
[here](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/replication_paper/arxiv_draft/appendix.pdf).

Version 1.1 is the most recent version and was posted on
[ArXiv](https://arxiv.org/abs/2202.07081) on July 26, 2022. Version 1.0
was posted on February 15, 2022.

## The Data:

The agreed datasets are the final dataset used in much of the paper and
figures. It includes our best efforts at cleaning the data and
reconciling intercoder agreement. The dataset is available in long and
wide format. The data is also available in .tsv format in the same
folders.

-   [ICBe_V1_long.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_long_agreed.Rds)
-   [ICBe_V1.1_long_agreement.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_wide_agreed.Rds)
    -   All coded values individually along with information about how
        often they were selected by coders.  
    -   `ICBe_V1_long.Rds` filtered down only to those codings that were
        agreed upon (see Algorithm 1 in paper).
-   [ICBe_V1.1_events_agreed_long.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_wide_agreed.Rds)
    -   [ICBe_V1.1_events_agreed.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_wide_agreed_long.Rds)

        -   `ICBe_V1.1_events_agreed.Rds` in wide form where each row is
            an event.

The coding and cleaning process are described in the paper with
additional information and details about the variables in the
codebook. - [ICBEdataset
Codebook](https://docs.google.com/document/d/1aJkweohbfIWtNpJw1CmXbeIiK6czbJ5iPyKwiYP1YlU/edit?usp=sharing)

## The Authors:

[Rex W. Douglass](http://www.rexdouglass.com), [Thomas Leo
Scherer](http://tlscherer.com/), [J. Andrés
Gannon](https://jandresgannon.com/), [Erik
Gartzke](http://erikgartzke.com/), [Jon
Lindsay](https://www.jonrlindsay.com/), [Shannon
Carcelli](https://www.shannoncarcelli.com/), Jonathan Wilkenfeld, David
M. Quinn, Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle
Murauskaite, and Diana Partridge.

## Citation:

For any use of the dataset or paper, please cite:

Douglass, Rex W., Thomas Leo Scherer, J. Andrés Gannon, Erik Gartzke,
Jon Lindsay, Shannon Carcelli, Jonathan Wiklenfeld, David M. Quinn,
Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle
Murauskaite, and Diana Partridge. 2022. “Introducing the ICBe Dataset:
Very High Recall and Precision Event Extraction from Narratives about
International Crises.” arXiv:2202.07081 \[cs, stat\].
<http://arxiv.org/abs/2202.07081>.

## Replication Code and Analysis

A description of the file and folders in the repository used to create
the datasets, tables, figures.

## data preparation

### replication_corpus

-   download_and_clean
    -   creates a succinct rds of the crisis narratives:
        `.replication_corpus/data/out/icb_corpus_V1.0_May_16_2022`

### replication_data

-   01_compile_saves_and_align
    -   compiles the original coding files into
        `./replication_data/in/icb_long_spans.Rds`. The original coding
        files are not on the public repository. Public users will load
        `icb_long_spans.Rds` directly.
    -   aligns codings from multiple GUI versions on similar source
        sentences
-   02_format_and_clean
    -   applies cleaning dictionaries to create
        `./replication_data/out/ICBe_V1.1_long_clean.Rds`.
-   03_aggregation
    -   applies aggregation algorithm to create
        `./replication_data/out/ICBe_V1.1_long_agreement.Rds`,
        `ICBe_V1.1_long.Rds`,
        `./replication_data/out/ICBe_V1.1_events_agreed.Rds`,
        `./replication_data/out/ICBe_V1.1_events_agreed_long.Rds`.
-   04_validation
    -   applies iconography to crises and events to create
        `ICBe_V1.1_crises_markdown.Rds` and
        `ICBe_V1.1_events_agreed_markdown.Rds`

### replication_paper

The figures are created in Rmd file for the paper
(./replication_paper/pnas_draft/ICBe_pnas_submission_rmd.Rmd). In some
cases they have been transformed to other formats via GNU Image
Manipulation Program.

-   `case_study_cuban_precision.png`
-   `recall_cuban_and_crimea_andcounts.png`
    -   Draws from the [Cuban Missile Automated Case Study
        googlesheet](https://docs.google.com/spreadsheets/d/1NuRWFB1HEbQbJu_JoEzJ9WYk7kfwwCryF7wBfKPT6uc/edit?usp=sharing)
        and the [Crimea-Donbas Automated Case Study (redone)
        googlesheet](https://docs.google.com/spreadsheets/d/1YesAx1CkYCgrEi_WVJ9aho60HesWA6p-3XMma9IzBrI/edit?usp=sharing).
    -   uses the iconographry in `./replication_data/in/flags_small/`
-   `p_precision_combined.png`
    -   combines metro maps of the two case studies using
        ICBe_V1.1_events_agreed.Rds
-   `p_semantic_embeddings_dendro.png`
    -   plot of semantic embeddings of
        ICBe_V1.1_events_agreed_markdown.Rds
-   `p_precision_icews.png`
    -   mapping of icews using
        `./replication_paper/data/out/icews_clean_471_lowest.tsv`
        (created in `./replication_paper/pnas_draft/appendix.Rmd`)

## Data inputs:

### ICBe preparation

-   Cleaning dictionaries: used to clean raw codings for actors,
    actions, locations, and dates
    `/replication_paper/data/in/icb_manual_recording_master_sheet.xlsx`
-   Lit review and tree/leaf codebook:
    `replication_data/in/icbe_litreview_trees_sentences.xlsx` and
    `/replication_paper/data/in/icbe_litreview_trees_sentences.xlsx`
-   Case study tables: `/replication_paper/data/in/CaseStudies.xlsx`

### External datasets

-   [The ICB project](https://sites.duke.edu/icbdata/)
    -   System-level (icb1v14.csv) and Actor-level (icb2v14.csv)
        datasets
    -   Dyadic-Level Crisis Data
        ([source](https://sites.duke.edu/icbdata/data-collections/))
-   [Militarized Interstate Disputes
    (MID)](https://correlatesofwar.org/data-sets/MIDs) version 5.01 at
    the incident level (MIDI_5.01.Rds) and incident-participant level
    (MIDIP_5.01.Rds) converted to Rds.
-   [UCDP Georeferenced Event Dataset (GED) Global version
    21.1](https://ucdp.uu.se/downloads/index.html#ged_global)
    (GEDEvent_v23_1.RData)
-   Cameo Event Codes adapted from [CAMEO Conflict and Mediation Event
    Observations
    Codebook](https://parusanalytics.com/eventdata/cameo.dir/CAMEO.09b6.pdf)
    (cameo.eventcode.txt)
-   [Phoenix Event
    data](https://databank.illinois.edu/datasets/IDB-2796521)
-   [Terrier event data](https://osf.io/4m2u7/files/)
    -   too large to include in the github repository
    -   to replicate, download the folder ‘largegeolocatedata’ to
        ICBEdata/replication_paper/data/ignore and decompress
-   [ICEWS
    data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/28075&version=30.0)
    -   too large to include in the github repository
    -   to replicate, download folder ‘dataverse_files’ to
        ICBEdata/replication_paper/data/ignore/ and decompress

### Appendix

The v1.1 Online Appendix can be downloaded
[here](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/raw/master/replication_paper/arxiv_draft/appendix.pdf).

### License and DOI

This work is licensed under a [Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International
License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

[![CC BY-NC-SA
4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

[![DOI](https://zenodo.org/badge/450249483.svg)](https://zenodo.org/badge/latestdoi/450249483)
