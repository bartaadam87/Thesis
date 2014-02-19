TEX = pdflatex
BIB = biber

.PHONY: all view

all : master_thesis.pdf

view :
	okular master_thesis.pdf

master_thesis.pdf : master_thesis.tex master_thesis.bbl master_thesis.blg
	$(TEX) master_thesis.tex

master_thesis.bbl master_thesis.blg : literatura.bib master_thesis.aux
	$(BIB) master_thesis

master_thesis.aux : master_thesis.tex
	vlna -v KkSsVvZzOoUuAaIi master_thesis.tex
	$(TEX) master_thesis.tex

master_thesis.bib : master_thesis.tex
	$(TEX) master_thesis.tex

clean :
	rm -f master_thesis.aux
	rm -f master_thesis.blg
	rm -f master_thesis.bbl
	rm -f master_thesis.toc
	rm -f master_thesis.log
	rm -f master_thesis.out
