# CIVL-GAP

This is an experiment to see if I can reproduce the CIVL GAP scoring docs,
starting from LaTeX markup.

Scoring is not simple. Hang-gliding and paragliding are scored similarly but
there are quite a few differences. Over the years scoring has evolved and it is
getting more complex. I'm not sure about this but I expect that only the latest
rules are documented.

## Getting Started

The whole document can be compiled and typeset to `*.pdf` on the command line
with;

```
> xelatex gap.tex
This is XeTeX, Version 3.14159265-2.6-0.99998 (TeX Live 2017) (preloaded format=xelatex)
...
Output written on gap.pdf (48 pages).
Transcript written on gap.log.
```

This `gap.tex` document can be loaded into a LaTeX editor but working on the
document as a whole can take a lot longer to compile than working on a section
by itself. Any of the sections can be compiled individually either in an editor
or on the command line.

```
> xelatex sec-philosophy.tex
This is XeTeX, Version 3.14159265-2.6-0.99998 (TeX Live 2017) (preloaded format=xelatex)
...
Output written on sec-philosophy.pdf (3 pages).
Transcript written on sec-philosophy.log.
```

Sections are those files prefixed with `sec-` such as `sec-philosophy.tex`. The
other `*.tex` files contain diagrams and graphs.

Note that typesetting the document as a whole must be made twice to create and
then reference labels for sections, figures and tables. On the first pass these
references will be rendered as **??**.

## Why LaTeX?

> ### LaTeX – A document preparation system

> LaTeX is a high-quality typesetting system; it includes features designed
> for the production of technical and scientific documentation. 

> LaTeX is the de facto standard for the communication and publication of
> scientific documents. LaTeX is available as free software.

SOURCE: [https://www.latex-project.org/](https://www.latex-project.org/)

LaTeX has markup for equations and charts. Its plain-text source works in well
with source control and related tooling.

GAP scoring is well documented.  Currently, the source format is *.docx and it
is published as a single *.pdf file,
[Sporting Code Section 7A - Annex GAP - Edition 2018](https://www.fai.org/sites/default/files/civl/documents/sporting_code_s7a-xc-civl_gap_2018.pdf),
running to about fifty pages with very many equations and quite a few charts.

### From Implementation, for Implementers and for Scorers.

Some of the documentation has surely been written about after being implemented
and some of what is implemented has no documentation. There are places where
readers are advised to consult the code and warned that the code differs from
the rules or worse yet that we're not sure what the code does exactly.

### Collaboration

Having the documentation in LaTeX could help.  A contributor finding an issue
could reference and highlight a line number range in the source. Authors could
work at the same time on different parts of it without having conflicts and if
their contributions do overlap then there is merge tooling for resolving
conflicts.  Version history, differences, tagged versions and published
releases are also available.
