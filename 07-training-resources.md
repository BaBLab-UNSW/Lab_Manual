# Section 7: Training Resources

## MRI / fMRI Analysis

- **[Andy's Brain Book](https://andysbrainbook.readthedocs.io/)** — the best starting point for anyone new to fMRI analysis. Free, self-paced, and walks through a full analysis from raw data to results using FSL, AFNI, or SPM (pick whichever your project uses - we use FSL typically). Also has dedicated tutorials on BIDS and fMRIPrep (see below).
- **[FSL Course materials](https://fsl.fmrib.ox.ac.uk/fslcourse/)** (Oxford FMRIB/WIN) — the in-person course has a fee, but Oxford posts the full lecture recordings, slides, and practicals from past courses online for free, including an "Introduction to Neuroimaging Analysis" primer that's a good first read before touching FSL itself.
- **[BIDS Starter Kit](https://bids-standard.github.io/bids-starter-kit/)** — the Brain Imaging Data Structure is the standard way to organise raw MRI data now, and most modern pipelines (fMRIPrep, MRIQC) expect it. Worth doing before you collect a single scan on a new study, not after.
- **fMRIPrep tutorials** — [Andy's Brain Book's fMRIPrep walkthrough](https://andysbrainbook.readthedocs.io/en/latest/OpenScience/OS/fMRIPrep.html) and the [Carpentries Incubator lesson on exploring fMRIPrep outputs](https://carpentries-incubator.github.io/SDC-BIDS-fMRI/02-exploring-fmriprep.html) are both free and hands-on.
- **[Neurohackademy](https://neurohackademy.org/)** (University of Washington) — a two-week summer institute whose lecture recordings and tutorial materials (Python, reproducibility, Git/GitHub, neuroimaging data science) are posted freely online every year, also indexed on [INCF TrainingSpace](https://training.incf.org/course/neurohackademy).
- **[The Princeton Handbook for Reproducible Neuroimaging](https://brainhack-princeton.github.io/handbook/)** — less a course, more a practical reference for doing neuroimaging analysis reproducibly (directory structure, pipelines, common pitfalls).

## Microbiome Bioinformatics (QIIME 2)

- **[Microbiome Bioinformatics with QIIME 2 — free online workshop](https://workshops.qiime2.org/microbiome-bioinformatics-qiime-2-free-online-work/)** — the official QIIME 2 team's ~12-hour workshop, released free with recorded lectures and hands-on tutorials, covering import/demultiplexing/denoising through diversity analyses. Also on [YouTube](https://www.youtube.com/playlist?list=PLbVDKwGpb3XmkQmoBy1wh3QfWlWdn_pTT).
- **[QIIME 2 Current Protocols documentation](https://curr-protoc-bioinformatics.qiime2.org/)** — a more formal, citable end-to-end walkthrough of a complete microbiome analysis, good as a reference once you've done the workshop.
- **[QIIME 2 Forum](https://forum.qiime2.org/)** — genuinely useful for troubleshooting; the developers and community answer questions directly, and it's searchable for issues you'll likely hit early on.

## R (general, and for stats/reproducible analysis)

- **[Learning Statistics with R](https://learningstatisticswithr.com/)** (Danielle Navarro) — a full, free, open-licence textbook aimed specifically at psychology students learning R and statistics together. Probably the single best starting point for anyone in the lab who is new to both R and stats.
- **[R for Data Science (2nd ed.)](https://r4ds.hadley.nz/)** (Wickham & Grolemund) — free online, the standard reference for the tidyverse approach to importing, cleaning, and visualising data in R. Good next step once you're comfortable with the basics.
- **[Data Carpentry / Software Carpentry R lessons](https://datacarpentry.org/)** — free, self-paced, workshop-style lessons that assume no prior programming experience; also cover the command line and Git, which pairs well with the reproducibility practices in Section 3.
- **[swirl](https://swirlstats.com/)** — an R package that teaches R interactively inside the R console itself (install it, run `swirl()`, and it walks you through exercises with immediate feedback). Good for people who learn better by typing than by reading.
- **[Tidyverse Style Guide](https://style.tidyverse.org/)** — the style guide the lab's code conventions are based on (see Data Analysis & Code Practices). Pair it with the `styler` package, which will reformat existing code to match automatically.
- **[Advanced R](https://adv-r.hadley.nz/)** (Wickham) — free online, for once you're past the basics and want to understand how R actually works under the hood (useful once you're writing your own functions rather than just running analyses).
- **A very basic tutorial for performing linear mixed effects analyses** ([Bodo Winter, PDF](https://jontalle.web.engr.illinois.edu/MISC/lme4/bw_LME_tutorial.pdf)) — the tutorial most people in developmental/cognitive psychology cite as their entry point into `lme4` and mixed models; short, practical, and aimed at exactly this kind of repeated-measures/nested data.

If you find other free resources that were useful to you, add them to this section — this list should keep growing as tools change.
