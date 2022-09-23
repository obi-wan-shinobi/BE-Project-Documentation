PDFLATEX=pdflatex -interaction=nonstopmode -halt-on-error
all: ml-astro22.pdf

%.pdf: %.tex references.bib
	- $(PDFLATEX) $(@:%.pdf=%) > $(@:%.pdf=%.log)
	- biber $(@:%.pdf=%)
	- $(PDFLATEX) $(@:%.pdf=%) > $(@:%.pdf=%.log)
	$(PDFLATEX) $(@:%.pdf=%)
