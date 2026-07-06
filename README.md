# Internship Report — LTI (2026)

Curricular internship report for the Bachelor's Degree in Information Technologies (ESTGA-UA).
Topic: *Evolution of a Maritime Monitoring System: SeaRates API Integration*.

## How to compile

```bash
latexmk -pdf main.tex
```

```bash
latexmk -C main.tex
latexmk -pdf main.tex
```

This command automatically handles the `pdflatex` → `biber` → `pdflatex` → `pdflatex` passes
needed to resolve citations, cross-references, table of contents, and bibliography.

### Prerequisites

- MiKTeX (or TeX Live) with the following packages:
  - `babel` (portuguese), `csquotes`, `biblatex` (IEEE), `acronym`
  - `newtxtext`, `newtxmath`
  - `fancyhdr`, `titlesec`, `setspace`, `geometry`
  - `graphicx`, `float`, `caption`, `chngcntr`
  - `booktabs`, `array`, `multirow`
  - `hyperref`, `url`, `xcolor`, `listings`
  - `appendix`, `pdfpages`
- `biber` (for bibliography — included with MiKTeX/TeX Live)
- `latexmk` (included with MiKTeX/TeX Live)

### Root file

- `main.tex` — root document. Do not compile other `.tex` files directly.

### Project structure

| File/Folder           | Description                                      |
|------------------------|--------------------------------------------------|
| `main.tex`             | Root document (cover, body, appendices)          |
| `references.bib`       | Bibliography in biblatex format (IEEE)           |
| `images/`              | Images and logos                                 |
| `out/`                 | Build auxiliary output                           |

### Notes

- The bibliography style is **IEEE** (`biblatex` with `style=ieee, sorting=none`).
- Figure and table numbering is continuous (not per chapter).
- Appendices use the `appendix` package with Portuguese redefinitions.
- `latexmk` is configured to automatically run `biber` when needed.
