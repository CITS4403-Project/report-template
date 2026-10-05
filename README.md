# CITS4403 Report Template

A LaTeX template for the CITS4403 Computational Modelling research project
report (UWA). It provides a ready-to-build document with one file per report
section, bibliography and figure scaffolding, and build rules for `latexmk`.

## Requirements

A LaTeX distribution that provides `latexmk` and `pdflatex`:

- **Linux:** `sudo apt install latexmk texlive-latex-recommended texlive-latex-extra` (or the full TeX Live)
- **macOS:** MacTeX
- **Windows:** MiKTeX or TeX Live

## Using this template

Create your own repository from this template with the **Use this template**
button on GitHub, or from the command line:

```bash
gh repo create <your-repo> --template CITS4403-Project/report-template --private
```

Alternatively, clone it directly:

```bash
git clone https://github.com/CITS4403-Project/report-template.git
```

## Building

```bash
make             # build build/report.pdf and refresh report.pdf
make watch       # rebuild automatically while editing (Ctrl-C to stop)
make clean       # remove intermediate build files
make distclean   # also remove the generated report.pdf
```

Intermediate files are written to `build/`. The finished report is copied to
`report.pdf` in the repository root, which is committed so the latest compiled
version is always available. Run `make` and commit `report.pdf` alongside any
source changes before merging.

## Structure

```
.
+-- report.tex       % main document (preamble, title, abstract, includes)
+-- report.pdf       % compiled report (committed; refreshed by make)
+-- sections/        % one file per report section
+-- references.bib   % BibTeX references
+-- figures/         % figures included in the report
+-- Makefile         % build rules
```

The section files map onto the assessment criteria: background and research
aims, originality and contribution, model specification, experimental design,
results, and discussion/conclusions.

## Formatting requirements

From the unit specification:

- maximum **five A4 pages**, excluding figures, references and appendices;
- **11pt font** and **1-inch margins** on all sides.

The preamble already sets `11pt` and 1-inch margins. Keep long derivations,
extra figures and parameter tables in the appendix so the main body stays
within the page limit.

## Workflow

1. Create a branch for your changes, for example `git checkout -b intro-background`.
2. Commit in small, single-line commits with clear messages.
3. Open a pull request for review before merging into `main`.