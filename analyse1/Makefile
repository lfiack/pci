FILE	= main
TEX = $(wildcard *.tex)
TITLE = title
#FIG = ../../figures/
#DIA = $(wildcard $(FIG)*.dia)

#.PRECIOUS : $(EPS)

all: $(FILE).pdf

$(FILE).pdf: $(TEX) $(FILE).tex $(TITLE).tex # $(FILE).bib # $(DIA) biblio.bib
#	make -C $(FIG)
	pdflatex $(FILE).tex
#	bibtex $(FILE)
#	pdflatex $(FILE).tex
	pdflatex $(FILE).tex

okular: $(FILE).pdf
	okular $(FILE).pdf &

evince: $(FILE).pdf
	evince $(FILE).pdf &

clean:
#	make -C $(FIG) clean
	rm -f $(FILE).aux $(FILE).log $(FILE).out $(FILE).toc 
	rm -f $(FILE).bbl $(FILE).blg $(FILE).idx
	rm -f $(FILE).maf  $(FILE).mtc $(FILE).mtc0

mrproper: clean
	rm -f $(FILE).pdf
