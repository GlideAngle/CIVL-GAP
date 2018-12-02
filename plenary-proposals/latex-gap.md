# LaTeX for GAP

A proposal for the CIVL Plenary Meeting 2019

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
a problem with that but I see a process with more friction than the alternative
I'm about to propose for making other kinds of change. Here I'm thinking of
insubstantial changes such as fixing typos, improving grammar, correcting
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
github. This is how I propose the process of making changes to the GAP annex
would then work:

The repository remains public. Anyone finding a small problem such as a typo
can raise an issue or make a pull request immediately with the correction. For
more substantial changes raising an issue is still a good idea. It is even
possible to provide templates for such issues, basically a checklist of things
to do when lodging the issue. For these larger changes, the repository would
need to be forked and we'd require the work to be done on a branch. The reason
for branching is to fit in with the current formal proposal and review process.
The changes can be seen by comparing branches, in this case between **master**
and the branch with the proposed changes. If the proposal is accepted as-is
then it can be merged when accepted. If it requires more work then these
changes can be made on the branch. They get added to any existing pull request
on that branch anyway.

I'm a software developer and [contribute to many
projects](https://ghuser.io/philderbeast) hosted on github but these days many
non-technical groups are using github for collaboration.  There's even a video
tutorial series called [Git and GitHub for
Poets](https://www.youtube.com/watch?v=BCQHnlnPusY&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV).

GitHub really has a great web interface. A contributor finding an issue can
reference and highlight a line number range in the source. Authors can work at
the same time on different parts of the GAP annex without having conflicts and
even if their contributions do overlap then there is merge tooling for
resolving such conflicts.  Version history, differences, tagged versions and
published releases are also available.

By holding off merging changes until they undergo formal review at a plenary
we'd also be able to accommodate the current formal process with this solution.
