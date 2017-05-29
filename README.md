This repository contains the draft documents for the Revised⁷ Report
on Scheme--Large, a set of libraries that provide a “batteries
included” facility for Scheme implementations. The process of
producing these reports involves taking the various SRFIs
(http://srfi.schemers.org) proposing libraries, and organizing them
into a standard report format.

This repository is NOT intended, at present, for end-users. The
documents here are not yet definitive, and are at varying stages of
pre-production.

At present, the Red Edition is the only document provided. To build
it, you will need a current TeX distribution (TeX Live or MiKTeX, for
example). Issuing a bare `make' command will build a PDF in
output/r7rs-large-red.pdf.

Contrary to the normal rule about not checking in build artifacts, the
PDF result appears at the top level, so that you can read the draft
without building it.

The process of grabbing the SRFIs and converting them to LaTeX is
semi-automated. YOU ONLY DO THIS ONCE; after that, all the editing is
done on the LaTeX files. The directory `scripts' contains two tiny
scripts that download the SRFIs and then convert them to LaTeX. You
will need wget and pandoc to make this work. Create a file named
spec.tex which contains whatever you like, but contains lines like

  \includesrfi{1234}

Then incant `make initial'. This downloads the SRFIs into a directory
named `srfi', and then produces LaTeX versions in `srfi-tex'. Now copy
those files into `srfi-edited', and you're off! 