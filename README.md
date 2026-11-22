# NDS Exposé Layout
[![Document Build](https://github.com/RUB-NDS/exposee_layout/actions/workflows/compile-thesis.yml/badge.svg)](https://github.com/RUB-NDS/exposee_layout/actions/workflows/compile-thesis.yml)

Latex template for students writing an exposé for a seminar, bachelor or master thesis.

## Quick start

1. Open this repository in VSCode with the *Dev Containers* extension and re-open in container.
   The devcontainer ships with TeX Live, latexmk, the LTeX grammar/spell checker and an inline PDF viewer.
2. Edit [`settings.tex`](settings.tex): type, title, author, examiners, date.
3. Write your chapters in [`chapters/`](chapters/) and your bibliography in [`literature/literature.bib`](literature/literature.bib).
4. Save any `.tex` file and the container builds the PDF automatically.

## Repository layout

| Path | Purpose |
|---|---|
| [`exposee.tex`](exposee.tex) | Main entry point. Lists which chapters are included. |
| [`settings.tex`](settings.tex) | All exposé-specific values (edit this). The same file works in the [thesis template](https://github.com/RUB-NDS/thesis_layout). |
| [`template/`](template/) | Title page, declaration, bibliography. **Do not edit unless you know what you are doing.** |
| [`chapters/`](chapters/) | One file per chapter, plus `abstract.tex` and the Gantt charts. |
| [`glossary/glossary.tex`](glossary/glossary.tex) | Acronyms and glossary entries. |
| [`literature/literature.bib`](literature/literature.bib) | BibTeX bibliography. |
| [`forms/declaration.pdf`](forms/declaration.pdf) | Declaration of authorship (form of the Faculty of Computer Science). Its text fields can be filled in in the built PDF. Sign it after printing. |
| [`images/`](images/) | Logos and figures. |
| [`examples/`](examples/) | Exposés of former students. |

## Building manually

```sh
latexmk -pdf exposee.tex
```

With older TeX Live versions, the `minted` package additionally needs `--shell-escape`.

The PDF of the latest build: [exposee.pdf](https://github.com/RUB-NDS/exposee_layout/releases/latest/download/exposee.pdf).
