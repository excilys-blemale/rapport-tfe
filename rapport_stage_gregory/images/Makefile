FICHIERS_DIA=$(wildcard *.dia)
FICHIERS_FIG=$(wildcard *.fig)
FICHIERS_EPS=$(wildcard *.eps)
FICHIERS_PNG=$(wildcard *.png)
FICHIERS_JPG=$(wildcard *.jpg)
FICHIERS_GIF=$(wildcard *.gif)
FICHIERS_PDF=$(FICHIERS_DIA:.dia=.pdf) $(FICHIERS_FIG:.fig=.pdf) $(FICHIERS_EPS:.eps=.pdf) $(FICHIERS_PNG:.png=.pdf) $(FICHIERS_JPG:.jpg=.pdf) $(FICHIERS_GIF:.gif=.pdf)
.SUFFIXES : .pdf .eps .tex .fig .dia .png .jpg .gif

all: ${FICHIERS_PDF}

.gif.pdf:
	convert $*.gif $*.pdf

.png.pdf:
	convert $*.png $*.pdf

.jpg.pdf:
	convert $*.jpg $*.pdf

.eps.pdf:
	epstopdf $*.eps

.fig.pdf:
	fig2dev -L pdf $*.fig $*.pdf

.dia.eps:
	dia --export=$*.eps --filter=eps-pango $*.dia

clean:
	rm -f ${FICHIERS_PDF}
