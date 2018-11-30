# CIVL-GAP

This is an experiment to see if I can reproduce the CIVL GAP scoring docs,
starting from LaTeX markup.

Scoring is not simple. Hang-gliding and paragliding are scored similarly but
there are quite a few differences. Over the years scoring has evolved and it is
getting more complex. I'm not sure about this but I expect that only the latest
rules are documented.

## Getting Started

Clone this repository, open a shell and typeset `gap.tex` to produce `gap.pdf`.

```
> git clone https://github.com/BlockScope/CIVL-GAP.git
> cd CIVL-GAP
> xelatex gap.tex
This is XeTeX, Version 3.14159265-2.6-0.99998 (TeX Live 2017) (preloaded format=xelatex)
...
Output written on gap.pdf (48 pages).
Transcript written on gap.log.
```

I edit the various `*.tex` document fragments in a plain text editor but there
are tools such as [TeXworks](https://en.wikipedia.org/wiki/TeXworks) that are
purpose-built for editing LaTeX and for typsetting and previewing the resultant
`*.pdf`. It runs on Windows, Linux and OSX and is free but requires a separate
TeX installation. For this, I've used
[MiKTeX](https://en.wikipedia.org/wiki/MiKTeX) on Windows and
[MacTeX](https://en.wikipedia.org/wiki/MacTeX) on OSX. The editing experience
is not [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) with TeXworks, it has
separate windows for editing the source file and for showing the preview.

The whole document can be worked on at once by loading `gap.tex` into the
editor but it is quicker to work on only a section at a time. Each section has
its own `sec-*.tex` file, `sec-introduction.tex` for example. Each appendix is
also self-contained in this way but named `apx-*.tex` such as
`apx-gap-defaults.tex`. Individual sections can be typeset from the command
line too.

```
> xelatex sec-philosophy.tex
This is XeTeX, Version 3.14159265-2.6-0.99998 (TeX Live 2017) (preloaded format=xelatex)
...
Output written on sec-philosophy.pdf (3 pages).
Transcript written on sec-philosophy.log.
```

Other `*.tex` files contain the LaTeX source for diagrams and graphs.

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

# Proposal for the CIVL Plenary Meeting 2019

## The Problem

> A Proposal shall include:
>
> * Your explanation of the problem and justification of the proposed solution,
> * Quotation of the old wording from Section 7 (if any) with paragraph number.
> * The new version of the wording to be put to Section 7 with the paragraph number.

From the [instructions on preparing
a proposal](https://www.fai.org/news/civl-plenary-2019) for making a change to
Section 7 of the FAI Sporting code.

This is a process for formal submission and review of substantial changes to
the sporting code (Section 7) or its GAP annex (Section 7a). I don't have
a problem with that but I see that process having too much friction compared to
the alternative I propose for making other kinds of change. Here I'm thinking
of insubstantial changes such as fixing typos, improving grammar, correcting
mistakes in formulae and drawing better diagrams and graphs.

Having reimplemented GAP in
[flare-timing](https://github.com/BlockScope/flare-timing) and working almost
exclusively from the GAP annex, I would like to see the explanation of how GAP
works improved.

Some of the documentation of how GAP works in the GAP annex (Section 7a) has
surely been written about after being implemented in the scoring software and
some of what is implemented has no documentation.  There are places where
readers are advised to consult the code and warned that the code differs from
the rules or worse yet that we're not sure what the code does exactly.

## The Solution

By nature, the GAP annex is a technical document with many formulae and some
diagrams and graphs. The solution I propose is to reuse what I have trialed in
this repository for producing the GAP annex (Section 7a) PDF document and
retire the existing `*.docx` source document. I would transfer ownership of
this repository to the [FAI-CIVL](https://github.com/FAI-CIVL) organization on
github. This is how I propose changes to the GAP annex would then work:

The repository remains public. Anyone finding a small problem such as a typo
can raise an issue or make a pull request with the correction. For more
substantial changes raising an issue is still a good idea. It is even possible
to provide templates for such issues, basically a checklist of things to do
when lodging the issue. For these larger changes, the repository would need to
be forked and we'd require the work to be done on a branch. The reason for
branching is to fit in with the current formal proposal and review process. The
changes can be seen by comparing branches, in this case between **master** and
the branch with the proposed changes. If the proposal is accepted as-is then it
can be merged immediately. If it requires more work then these changes can be
made on the branch.

I'm a software developer and contribute to many projects hosted on github but
these days many non-technical groups are using github for collaboration.
There's even a video tutorial series called **Git and GitHub for Poets**.
GitHub really has a great web interface. A contributor finding an issue can
reference and highlight a line number range in the source. Authors can work at
the same time on different parts of the GAP annex without having conflicts and
even if their contributions do overlap then there is merge tooling for
resolving such conflicts.  Version history, differences, tagged versions and
published releases are also available.

By holding off merging changes until they undergo formal review at a plenary
we'd also be able to accommodate the current formal process with this solution.
