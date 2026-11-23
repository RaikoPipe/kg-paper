# Draft project description (DFG Research Grant)

Draft built on the template in `../template` (unchanged). Structure follows DFG form 53.01 / 54.01 (09/26).

## Files
- `main.tex`: copy of the template main file. Two changes: `\input{template/header}` (path), and a second
  `\printbibliography` block for own preprints (`keyword=ownpreprint`), which the template did not print.
- `content/00_meta.tex`: applicants, title, names printed in bold.
- `content/01_aux_header.tex`: extra packages. Font: Helvetica clone with Arial metrics (`helvet` under pdfLaTeX,
  TeX Gyre Heros under XeLaTeX/LuaLaTeX), as form 54.01 asks for Arial 11 pt or comparable. Defines `\todo{}`.
- `content/04_starting_point.tex`: section 1 (state of the art, research gap, preliminary work of both sites).
- `content/06_objectives_and_work.tex`: section 2.1–2.4 (objectives, H1–H4, WP0–WP6, Gantt chart, staff table, risks, research data).
- `content/07_diversity.tex`, `08_supplement.tex`, `09_modules.tex`: sections 2.5, 4 and 5.
- `content/02_literature.bib`: generated from Crossref, DataCite and arXiv metadata (12 Nov 2026).
  `keywords={own}` (9 entries) and `keywords={ownpreprint}` (1 entry) give the 10 highlighted own works.
- `main.pdf`: compiled draft (18 pages; sections 1–3 = pages 1–11, limit 17; sections 4–5 = pages 12–18, limit 8).

## Build
```
latexmk -pdf main.tex        # pdfLaTeX + biber
# or: xelatex main && biber main && xelatex main && xelatex main
```
Requires biber (biblatex backend) and pgfgantt, tabularray (local copy), acronym, enumitem.

## Open TODOs (rendered in red)
About 30 `\todo{}` markers, mostly in sections 4 and 5: employment status and contract dates, first-time-proposal
data, project group, cooperation partners, completion of the co-author list, equipment, student-assistant hours
and rates, LLM API and travel amounts, publication costs, ethics committee requirements, AI-use statement,
official chair name in Dresden, list of planning cases and data permissions, co-authors of the GraphRAG preprint.

## Points to decide before submission
- Post the GraphRAG error-injection preprint (cited as [PRP1]); WP3 and WP4 rest on it.
- Confirm the joint proposal (Lang, Schmidt as applicants) and the WP split between sites.
- Staff costs use the DFG 2027 rate for doctoral researchers (EUR 83,700/year, form 60.12, 01/27); check the
  employment level recommended for the review board (form 55.02).
- The SLR is cited only as its OSF protocol; its numbers are described as own, unpublished results.
- ASMG4SimPy is described but not cited (unpublished).
