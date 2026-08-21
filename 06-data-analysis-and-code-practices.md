# Section 6: Data Analysis & Code Practices

Every analysis project in the lab — from an undergraduate's first script to the code behind a submitted paper — gets a GitHub repository, and every repository is expected to meet the same baseline.

### One repo per project

Each study or sub-project gets its own repository under the lab's GitHub organisation, named clearly (e.g. `mindbrainbody-interoception-followup`, not `analysis2` or `finalfinal`). Don't bury a project's code inside someone's personal miscellaneous repo — if you leave the lab, the project's code needs to be findable without you.

### What goes on GitHub, and what never does

Code goes on GitHub. **Raw or identifiable participant data never does — not even in a private repo.** GitHub is not an approved storage location for participant data under UNSW's data classification rules (see Data Access & Management); a repo being private doesn't change that. In practice:

- Scripts should read data from its actual location on OneDrive/SharePoint (or wherever the project's approved storage lives), referenced by a relative path, not a hardcoded path to a specific person's laptop.
- Add a `.gitignore` that explicitly excludes data folders, so a stray `git add .` can't accidentally commit a CSV full of participant responses. The lab manager can provide a standard `.gitignore` template — use it as your starting point for every new repo.
- If a repo genuinely needs example data to run (e.g., so someone else can test the pipeline), use a small simulated or fully de-identified synthetic dataset built for that purpose, clearly labelled as such.
- If you're ever unsure whether something is safe to commit, ask before pushing, not after.

### Script and repo structure

- Every repo has a `README.md` explaining, in plain language: what the project is, what each script does and the order to run them in, what the expected inputs and outputs are, and who to contact with questions. Link back to the study's wiki page rather than duplicating everything.
- Every script starts with a short header comment: what it does, who wrote it, when, and what it expects as input.
- Follow the [tidyverse style guide](https://style.tidyverse.org/) for formatting (the `styler` package will do most of this for you automatically) — consistency matters more than anyone's personal preference, because someone else will read this code.
- Use relative paths (e.g., via the `here` package) rather than absolute paths like `C:/Users/yourname/Desktop/`. A script that only runs on the machine that wrote it is not reproducible.
- Prefer R Markdown or Quarto documents over bare `.R` scripts for anything that produces reported results — narrative, code, and output living in one place makes it far easier for someone (including future-you) to follow what happened and why.

### Reproducibility mechanics

- Set a seed explicitly (`set.seed()`) anywhere randomness is involved (bootstrapping, permutation tests, train/test splits), and note why that seed and not another, if it matters.
- Record the analysis environment: run `sessioninfo::session_info()` at the end of your analysis and save the output alongside your results, so package versions are documented. For larger or long-running projects, use [`renv`](https://rstudio.github.io/renv/) to lock package versions for the whole project.
- Scripts should regenerate figures and tables from raw data through to the final output. If a figure in a paper was hand-edited after being exported from R, that's a red flag — the pipeline should produce the reportable output directly, or the manual edit should be documented and justified.

### Version control workflow

- Commit early, commit often, and write commit messages that explain *why*, not just *what* ("switch to robust SEs after reviewer comment" beats "update analysis.R").
- Use branches for exploratory or risky changes rather than working directly on `main`.
- Before merging any script that produces results going into a manuscript, thesis chapter, or conference presentation into `main`, have another lab member review it — run it themselves if possible, not just read it. This is the same "check it, then get someone else to check it" principle from Section 2, applied to code.
- When a manuscript is submitted, tag the exact commit that produced the reported results (e.g., `v1.0-submission`) so the analysis that generated a specific set of numbers stays addressable even as the code keeps evolving afterward. This also sets you up to mint a Zenodo DOI for the code release alongside the paper, consistent with the lab's open science policy (Section 5.8).

### Defaults on visibility

New analysis repos are private by default while a project is active (see Section 5.8, Open Science) and made public — ideally alongside a tagged, citable release — once Bridget agrees the lab is done working with it and it accompanies a preprint or publication. Don't make a repo public "to be safe" before that point.
