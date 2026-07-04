# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A **LaTeX academic paper** targeted at Elsevier's **Digital Business**:

> *Building Digital Resilience Through Vibe Coding: A Content Analysis of AI-Assisted
> Development for Sustainable Digital Transformation.*

A **directed (deductive) content analysis** of 97 sources — academic literature, industry
reports, developer-community discourse, and platform docs — read through an integrated lens of
**Dynamic Capabilities Theory**, the **Technology–Organization–Environment (TOE)** framework,
and **Diffusion of Innovation** theory. Core contributions: a *resilience paradox* (vibe coding
both strengthens and undermines organizational resilience), framing vibe coding as the **fourth
paradigm** of software-development automation (after CASE, the RAD/IDE/web-framework era, and
low-code), a tiered governance framework, and a bifurcated diffusion forecast to 2030.

- **Author:** Abdulhakeem Ibrahim (corresponding, hakeem.ibrahim@dmu.ac.uk), School of Computer
  Science and Informatics, De Montfort University, Leicester, UK. *(Sole author — Hongji Yang was
  removed from the author list; see git history.)*

## Build / compile

Main source is `manuscript.tex`; bibliography is `references.bib` (BibTeX, `elsarticle-harv`
style, `authoryear` citations). Output is `manuscript.pdf`.

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error manuscript.tex   # build manuscript.pdf
latexmk -c                                                            # clean aux files (keeps PDF)
```

After a content change, check `manuscript.log` for `Citation ... undefined` /
`Reference ... undefined` and `! ` (TeX error) lines.

**No compiler on `PATH`?** There is no MacTeX under `/Library/TeX/texbin` and nothing TeX-related
is on `PATH` by default, so a bare `latexmk`/`pdflatex` fails and `which pdflatex` finds nothing.
Before concluding "no compiler," use the local **TinyTeX** (TeX Live 2026) install at
`~/Library/TinyTeX/bin/universal-darwin/` — prepend it to `PATH` first:

```bash
export PATH="$HOME/Library/TinyTeX/bin/universal-darwin:$PATH"
latexmk -pdf -interaction=nonstopmode -halt-on-error manuscript.tex
```

TinyTeX is **minimal**, so a first build may fail on `File \`X.sty' not found` or a missing TikZ
library. It bundles `tlmgr` — install the missing piece on demand and rebuild:

```bash
tlmgr search --global --file "/xurl.sty"   # find which package ships a missing file
tlmgr install <package>                     # then re-run latexmk
```

> **Known-needed installs for this paper (verified 2026-07-04 on a fresh TinyTeX).** The
> `elsarticle` class and `elsarticle-harv` style are already bundled. A clean build of
> `manuscript.tex` additionally required:
> ```bash
> tlmgr install xurl adjustbox lineno pgf-blur
> ```
> `adjustbox` pulls in `collectbox`; `pgf-blur` provides the `shadows.blur` TikZ library used by
> the conceptual-model figure. `latexmk` drives the pdflatex → bibtex → pdflatex×2 passes
> automatically. The real success check is `grep '^! ' manuscript.log` (TeX errors) and
> `grep -c undefined manuscript.log` (0 after the final pass); the last clean build was 47 pages.

## Structure

`manuscript.tex` — `elsarticle` (`[preprint,12pt,authoryear]`), `\journal{Digital Business}`,
line numbers on (`\linenumbers`). Front matter has an abstract, keywords, and a 5-bullet
**Highlights** block (≤85 chars each; Digital Business wants these as a separate editable file at
submission). Sections: Introduction → Background and Theoretical Framework → Research Methodology
→ Findings → Discussion → Conclusion, Limitations, and Future Research, followed by the Elsevier
back-matter (CRediT, competing-interest, funding, data-availability declarations).

Figures are drawn inline with **TikZ** (`shapes.geometric, arrows.meta, positioning, calc, fit,
backgrounds, decorations.pathmorphing, shadows.blur`) — no external image files.

## Notes

- Compilation is regenerable: after a build, `manuscript.pdf/.aux/.bbl/.log/.fls/.fdb_latexmk`
  will show as modified in git. Commit the source (`manuscript.tex`, `references.bib`) and the
  refreshed `manuscript.pdf`; the other aux files are build artifacts.
- `manuscript.md` is a Markdown mirror of the paper; `resources/` and `fdgth-7-1656804.pdf` hold
  source/reference material. The `references/` folder of downloaded PDFs was removed (see git
  status) — the authoritative bibliography is `references.bib`.
