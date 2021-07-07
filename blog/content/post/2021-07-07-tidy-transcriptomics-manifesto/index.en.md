---
title: Tidy-transcriptomics manifesto
author: Stefano & Maria
date: '2021-07-07'
slug: []
categories:
  - all platforms
tags:
  - tidytranscriptomics
  - manifesto
  - transcriptomics
  - tidyverse
lastmod: '2021-07-07T14:16:36+10:00'
keywords: []
description: ''
comment: no
toc: no
autoCollapseToc: no
postMetaInFooter: no
hiddenFromHomePage: no
contentCopyright: no
reward: no
mathjax: no
mathjaxEnableSingleDollar: no
mathjaxEnableAutoNumber: no
hideHeaderAndFooter: no
flowchartDiagrams:
  enable: no
  options: ''
sequenceDiagrams:
  enable: no
  options: ''
---

<!--more-->
<img src="images/logo.png" alt="tidytranscriptomics_logo" width="300px" height="300px"/>

In this first post, we want to introduce the concept of tidy transcriptomics, and the principles is moved by.

# What is tidy transcriptomics
...

# The tidy transcriptomics manifesto


This document lays down the principles of tidy transcriptomics, of which `tidybulk` and `tidySummarizedExperiment`, `tidySingleCellExperiment`, and `tidyseurat` are based on. These principles are in line with [the tidy tools manifesto](https://cran.r-project.org/web/packages/tidyverse/vignettes/manifesto.html).

- **Use easy-to-understand, verbose, jargon- and acronym-free vocabulary.** If the English dictionary is not enough to understand the underlying meaning of a function or a variable name, it is a bad sign. Learning is incredibly slown-down by a cryptic vocabulary; and the cost of saving few characters is usually bigger than you think.
- **Present/visualise information in its raw form when possible.** Modern visualisation tools (e.g. ggplot) allow to use custom scales to visualise data. For example, for visualising p-values apply the `log10_reverse` scale instead of transforming the p-values in their negative-log form; for visualising (raw, scaled and/or adjusted) transcript abundance (in the form of read counts) use the `log1p` scale instead of transforming the data in its log (or count-per-million) form.
- **Avoid the creation of temporary variables when possible, and always avoid variable updating.** When working interactively, data-containing variables is a bug-prone process, especially if multiple assignments are done on the same variable though the workflow. The main utility of variables should be to store data that is used more than once. Tidyverse allows extremely complex operations in a functional way.
