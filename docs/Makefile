# Makefile for LaTeX template.

PDF=dt8122_probabilistic_ai_2019.pdf
VIEWER=$(shell which xdg-open open | head -n 1)

all: ${PDF}

%.pdf: %.tex
	latexmk -xelatex -bibtex $<
	${VIEWER} $@ &

clean:
	latexmk -c

veryclean: clean
	-rm ${PDF} *.bbl *.xdv
