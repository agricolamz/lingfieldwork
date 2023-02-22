# phonfieldwork

[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![](https://badges.ropensci.org/385_status.svg)](https://github.com/ropensci/software-review/issues/385)
[![CRAN version](http://www.r-pkg.org/badges/version/phonfieldwork)](https://cran.r-project.org/package=phonfieldwork)
[![](http://cranlogs.r-pkg.org/badges/grand-total/phonfieldwork)](https://CRAN.R-project.org/package=phonfieldwork)
[![R build status](https://github.com/ropensci/phonfieldwork/workflows/R-CMD-check/badge.svg)](https://github.com/ropensci/phonfieldwork/actions)
[![Coverage Status](https://img.shields.io/codecov/c/github/ropensci/phonfieldwork/master.svg)](https://codecov.io/github/ropensci/phonfieldwork?branch=master)
[![DOI](https://zenodo.org/badge/194053227.svg)](https://zenodo.org/badge/latestdoi/194053227)

`phonfieldwork` is a package for phonetic fieldwork research and experiments. This package makes it easier to:

- create a html/pptx presentation from stimuli-translation list, 
- rename soundfiles according to the list of stimuli, 
- concatenate multiple soundfiles and create a Praat TextGrid which interval labels are the original names of the sound
- extract sounds according to annotation
- extract annotation from multiple linguistic formats (Praat `.TextGrid`, ELAN `.eaf`, EXMARaLDA `.exb`, Audacity `.txt` and subtitles `.srt`)
- visualise oscilograms, spectrograms and annotations
- create an html viewer [like this](https://ropensci.github.io/phonfieldwork/additional/stimuli_viewer.html), ethical problems of this kind of viewer in linguistic research are covered in the vignette `vignette("ethical_research_with_phonfieldwork")`.

For more details see [tutorial](https://docs.ropensci.org/phonfieldwork/).

The main goal of the `phonfieldwork` package is to make the full research workflow, from data collection to data extraction and data representation, easier for people that are not familiar with programming. However, most of the `phonfieldwork` functionality can be found in other software and packages:

* stimuli presentation creation could be done with any programming language and probably without them
* automatic file renaming and automatic merging could be done with any programming language
* Praat `.TextGrid` manipulation is possible with Praat, R packages [`rPraat`](https://cran.r-project.org/package=rPraat) and [`textgRid`](https://cran.r-project.org/package=textgRid), Python package ['pympi'](https://dopefishh.github.io/pympi/index.html)
* ELAN `.eaf` manipulation is possible with ELAN, R package [`FRelan`](https://github.com/langdoc/FRelan) and Python package [`pympi`](https://dopefishh.github.io/pympi/index.html)
* import and export between Praat `.TextGrid`, ELAN `.eaf`, and 'EXMARaLDA .exb is possible with R package [`act`](https://cran.r-project.org/package=act)
* cutting sounds according to annotation is possible with Praat and the R package`tuneR`
* spectrogram visualisation is possible with multiple R packages [`signal`](https://cran.r-project.org/package=signal), [`tuneR`](https://cran.r-project.org/package=tuneR), [`seewave`](https://cran.r-project.org/package=seewave), [`phonTools`](https://cran.r-project.org/package=phonTools), [`monitor`](https://cran.r-project.org/package=monitor), [`warbleR`](https://cran.r-project.org/package=warbleR), [`soundgen`](https://cran.r-project.org/package=soundgen) and many others

## Installation

Install from CRAN:

```
install.packages("phonfieldwork")
```

Get the development version from GitHub:

```
install.packages("remotes")
remotes::install_github("ropensci/phonfieldwork")
```
Load the library:
```
library(phonfieldwork)
```

In order to work with some `rmarkdown` functions you will need to install `pandoc`, see `vignette("pandoc")` for the details.

## Cite the package

You can get the latest information about how to cite the package using the `citation()` function:

```
citation("phonfieldwork")
>
> To cite package ‘phonfieldwork’ in publications use:
>   
>   Moroz G (2020). _Phonetic fieldwork and experiments with phonfieldwork package_.
> <https://CRAN.R-project.org/package=phonfieldwork>.
> 
> A BibTeX entry for LaTeX users is
> 
> @Manual{,
>   title = {Phonetic fieldwork and experiments with phonfieldwork package},
>   author = {George Moroz},
>   year = {2020},
>   url = {https://CRAN.R-project.org/package=phonfieldwork},
> }
```

## To do:

* export to ELAN and EXMARALDA files
* use ELAN and EXMARALDA files in the whole pipeline described in docs
* use the same pipeline with video (for Sign Languages)
* make [TECkit](https://scripts.sil.org/cms/scripts/render_download.php?format=file&media_id=BeyondUTR22_pdf&filename=BeyondUTR22_pdf.pdf) to df and back

[![ropensci\_footer](https://ropensci.org/public_images/ropensci_footer.png)](https://ropensci.org)
