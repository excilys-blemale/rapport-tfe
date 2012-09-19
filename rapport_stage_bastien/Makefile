SHELL=/bin/bash
TEX=TEXINPUTS=$(TEXINPUTS):cls/:.

SORTIE=output
NOM=rapport

LATEX=$(NOM).tex
PDF=$(NOM).pdf

.SUFFIXES : .pdf .tex

all : $(SORTIE)/$(PDF) clean

$(SORTIE)/$(PDF) : $(PDF)
	[ -d "$(SORTIE)" ] || mkdir "$(SORTIE)"
	mv $< $@

.tex.pdf :
	make -C images
	$(TEX) pdflatex $*
	$(TEX) pdflatex $*

clean :
	rm -f *.aux
	rm -f *.cb
	rm -f *.cb2
	rm -f *.log
	rm -f *.out
	rm -f *.toc
	rm -f *~
	rm -f *.pdf
	rm -f *.backup
	rm -f *.pdf
	rm -f ./chapitres/*.aux
	rm -f ./chapitres/*.cb
	rm -f ./chapitres/*.cb2
	rm -f ./chapitres/*.log
	rm -f ./chapitres/*.out
	rm -f ./chapitres/*.toc
	rm -f ./chapitres/*~
	rm -f ./chapitres/*.backup
	rm -f ./chapitres/4_travail/*.aux
	rm -f ./chapitres/4_travail/*.cb
	rm -f ./chapitres/4_travail/*.cb2
	rm -f ./chapitres/4_travail/*.log
	rm -f ./chapitres/4_travail/*.out
	rm -f ./chapitres/4_travail/*.toc
	rm -f ./chapitres/4_travail/*~
	rm -f ./chapitres/4_travail/*.backup

clean-images :
	make -C images clean
