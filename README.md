MPEGKin
============================


[![DOI](https://zenodo.org/badge/374493336.svg)](https://zenodo.org/badge/latestdoi/374493336)


This repository contains the data from the MPEGKin project, which is included in the Kinbank project. 

Please use the following citation for this dataset:

Birchall, J., Araujo, L. H., Passmore, S., & Jordan, F. M. (2022). MPEGKin: A database of kinship terminology from the Tupian and Cariban language families [Data set]. Zenodo. https://doi.org/10.5281/zenodo.6474213


To add a new language:
----------------------

1. Add it to ./etc/languages.csv

2. Add a new csv file into ./raw/, using this format:

```csv:
parameter,word,ipa,description,alternative,source_raw,source_bibtex,comment
```

3. Add the reference into ./raw/sources.bib

4. Regenerate CLDF:

Run this shell command:

```shell
make cldf
```

To Generate a CLDF dataset:
---------------------------

The shell utility [make](https://www.gnu.org/software/make/) and the programming language [python (v3.6+)](https://www.python.org/) are required.

1. Install the python requirements:

The libraries needed for the python merge script are [cldfbench](https://pypi.org/project/cldfbench/0.2.0/) and [pylexibank](https://pypi.org/project/pylexibank/). These will be
installed into a virtual environment using this command:

```shell
make install
```

2. Generate CLDF:

```shell
make cldf
```
