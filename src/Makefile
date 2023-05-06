ROOT = main
BIBTEX = $(ROOT).aux
LATEX = latex
PDFLATEX = pdflatex
PDFLATEX_ARGS = -file-line-error -interaction nonstopmode -recorder --src-specials

all: distclean pdf clean

distclean: clean
	rm -f  *.pdf

clean:
	rm -f *~  *.log *.aux *.toc *.dvi *.bbl *.blg *.*~* *.lof *.lot *.cb *.backup *.out *.glo *.idx *.fls *.lol *.ilg *.gls *.plog *.ind *.npc *.nps *.nav *.fdb_latexmk *.snm *.vrb *.synctex.gz
	
pdf:
	$(PDFLATEX)  $(PDFLATEX_ARGS) $(ROOT)
	bibtex $(BIBTEX)
	$(PDFLATEX) $(PDFLATEX_ARGS) $(ROOT)
	$(PDFLATEX) $(PDFLATEX_ARGS) $(ROOT)
	$(PDFLATEX) $(PDFLATEX_ARGS) $(ROOT)
	mv ${ROOT}.pdf ../minicurso.pdf