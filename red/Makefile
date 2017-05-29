# Makefile for R7RS-large.

# Depends on everything, so no point in specifying dependencies.
r7rs-large-red.pdf:
	xelatex -output-directory output r7rs-large-red.tex
	# indexing comes later.

# This downloads all the SRFIs in the specification, and converts them to
# LaTeX format. You should only need to do this once. Requires wget and pandoc.
initial:
	scripts/getsrfis spec.tex
	scripts/html2tex
