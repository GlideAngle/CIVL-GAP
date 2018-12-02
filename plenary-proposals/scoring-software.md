# Setting the Bar for Software Scoring

I propose that CIVL set the bar for approving software used for scoring with
GAP.

I suggest the following list of requirements:

1. The program can read a common input format and produce a common output
   format, currently *.fsdb + *.kml + *.igc in and *.html out.
2. The code that does the scoring is open source. Other parts of the
   application can be closed.
3. There is somewhere to report and review issues with the code, eg. github
   issues.
4. There is a way to contribute fixes, eg. pull requests.
5. The scoring works on windows, linux and osx.
6. There are build instructions that work on windows, linux and osx.
7. There is documentation that explains the implementation.
8. There are releases with release notes and change logs and the source is
   tagged at release points.
9. The code that does the scoring can be run in isolation, apart from the
   application as a whole, in batch mode from the command line.
10. Working steps can be written to a file format that is human readable.
11. There are tests.
12. The build and tests are run on a public continuous integration service.

Points 1., 9. and 10. allow for a way to run the scoring program from the
command line (headless), reading common inputs and common outputs and allows
for scrutiny of the outputs and workings by humans.

Point 2. software that is open source allows for more scrutiny and is fairer
to pilots as nothing is hidden.

Points 5. & 6. makes an expectation that the software builds and runs on the
three most common operating systems around today.

Points 3., 4., 8., 11. and 12. are needed for onboarding and working with
contributors and scrutineers.

We cannot yet produce a set of automated tests that allow CIVL to pass or fail
an implementation of GAP but I think that is a worthy and reasonable goal.
