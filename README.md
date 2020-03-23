# ![nf-core/arctic](docs/images/nf-core-arctic_logo.png)

[![GitHub Actions CI Status](https://github.com/nf-core/arctic/workflows/nf-core%20CI/badge.svg)](https://github.com/nf-core/arctic/actions)
[![GitHub Actions Linting Status](https://github.com/nf-core/arctic/workflows/nf-core%20linting/badge.svg)](https://github.com/nf-core/arctic/actions)
[![Nextflow](https://img.shields.io/badge/nextflow-%E2%89%A519.10.0-brightgreen.svg)](https://www.nextflow.io/)

[![install with bioconda](https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg)](http://bioconda.github.io/)
[![Docker](https://img.shields.io/docker/automated/nfcore/arctic.svg)](https://hub.docker.com/r/nfcore/arctic)

## Introduction

The implementation of nf-core/arctic is an international collaboration between numerous contributors and developers. We appreciated the need to have a portable, reproducible and scalable pipeline for the analysis of COVID-19 sequencing samples and so the Avengers Assemble! Please come and join us and add yourself to the contributor list :)

This pipeline is a re-implementation of the amazing work already carried out by contributors to the [ARCTIC Network's field bioinformatics pipeline](https://github.com/artic-network/fieldbioinformatics) and their associated [bioinformatics protocol](https://artic.network/ncov-2019/ncov2019-bioinformatics-sop.html). [Matt Bull's Nextflow implementation]( https://github.com/connor-lab/ncov2019-artic-nf) was also used for some much needed inspiration.

The plan is to fully containerise and support both Nanopore (including demultiplexing) and Illumina (pre-demultiplexed) data in the same workflow.

The pipeline is built using [Nextflow](https://www.nextflow.io), a workflow tool to run tasks across multiple compute infrastructures in a very portable manner. It comes with docker containers making installation trivial and results highly reproducible.

## Quick Start

i. Install [`nextflow`](https://nf-co.re/usage/installation)

ii. Install either [`Docker`](https://docs.docker.com/engine/installation/) or [`Singularity`](https://www.sylabs.io/guides/3.0/user-guide/) for full pipeline reproducibility

iii. Download the pipeline and test it on a minimal dataset with a single command

```bash
nextflow run nf-core/arctic -profile test,<docker/singularity/institute>
```

> Please check [nf-core/configs](https://github.com/nf-core/configs#documentation) to see if a custom config file to run nf-core pipelines already exists for your Institute. If so, you can simply use `-profile <institute>` in your command. This will enable either `docker` or `singularity` and set the appropriate execution settings for your local compute environment.

iv. Start running your own analysis!

<!-- TODO nf-core: Update the default command above used to run the pipeline -->

```bash
nextflow run nf-core/arctic -profile <docker/singularity/conda/institute> --input samplesheet.csv
```

See [usage docs](docs/usage.md) for all of the available options when running the pipeline.

## Documentation

The nf-core/arctic pipeline comes with documentation about the pipeline, found in the `docs/` directory:

1. [Installation](https://nf-co.re/usage/installation)
2. Pipeline configuration
    * [Local installation](https://nf-co.re/usage/local_installation)
    * [Adding your own system config](https://nf-co.re/usage/adding_own_config)
3. [Running the pipeline](docs/usage.md)
4. [Output and how to interpret the results](docs/output.md)
5. [Troubleshooting](https://nf-co.re/usage/troubleshooting)

<!-- TODO nf-core: Add a brief overview of what the pipeline does and how it works -->

## Credits

| Name                                                      | Affiliation                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Alexander Peltzer](https://github.com/apeltzer)          | [Boehringer Ingelheim, Germany](https://www.boehringer-ingelheim.de/)                 |
| [Gisela Gabernet](https://github.com/ggabernet)           | [QBIC, University of Tubingen, Germany](https://portal.qbic.uni-tuebingen.de/portal/) |
| [Harshil Patel](https://github.com/drpatelh)              | [The Francis Crick Institute, UK](https://www.crick.ac.uk/)                           |
| [Matt Bull](https://github.com/m-bull)                    | [Public Health Wales, UK](https://phw.nhs.wales/)                                     |
| [Maxime Garcia](https://github.com/MaxUlysse)             | [SciLifeLab, Sweden](https://www.scilifelab.se/)                                      |
| [Nick Loman](https://github.com/nickloman)                | [University of Birmingham, UK](https://www.birmingham.ac.uk)                          |
| [Olga Botvinnik](https://github.com/olgabot)              | [Chan Zuckerberg Biohub, USA](https://www.czbiohub.org/)                              |
| [Phil Ewels](https://github.com/ewels)                    | [SciLifeLab, Sweden](https://www.scilifelab.se/)                                      |
| [Thanh Le Viet](https://github.com/thanhleviet)           | [Quadram Institute, UK](https://quadram.ac.uk/)                                       |
| [Will Rowe](https://github.com/will-rowe)                 | [University of Birmingham, UK](https://www.birmingham.ac.uk)                          |

> Listed in alphabetical order

## Contributions and Support

If you would like to contribute to this pipeline, please see the [contributing guidelines](.github/CONTRIBUTING.md).

For further information or help, don't hesitate to get in touch on [Slack](https://nfcore.slack.com/channels/arctic) (you can join with [this invite](https://nf-co.re/join/slack)).

## Citation

<!-- TODO nf-core: Add citation for pipeline after first release. Uncomment lines below and update Zenodo doi. -->
<!-- If you use  nf-core/arctic for your analysis, please cite it using the following doi: [10.5281/zenodo.XXXXXX](https://doi.org/10.5281/zenodo.XXXXXX) -->

You can cite the `nf-core` publication as follows:

> **The nf-core framework for community-curated bioinformatics pipelines.**
>
> Philip Ewels, Alexander Peltzer, Sven Fillinger, Harshil Patel, Johannes Alneberg, Andreas Wilm, Maxime Ulysse Garcia, Paolo Di Tommaso & Sven Nahnsen.
>
> _Nat Biotechnol._ 2020 Feb 13. doi: [10.1038/s41587-020-0439-x](https://dx.doi.org/10.1038/s41587-020-0439-x).  
> ReadCube: [Full Access Link](https://rdcu.be/b1GjZ)
