SDIR = Figures#.#sequence
MDIR = figures
EXTDIR = external

EPSPROG = epstopdf
FIGURES = $(SDIR)/rhoE.pdf $(SDIR)/rhoL.pdf
BIBFILES = 			

default: main.pdf
all: main.pdf
figures: $(FIGURES)

#intermediate.temp: main.tex main.bbl
#	pdflatex -draftmode -interaction=nonstopmode main.tex >intermediate.temp
	 
main.pdf: main.tex $(FIGURES)
	pdflatex -interaction=nonstopmode main.tex

#main.aux: main.tex
#	pdflatex -draftmode -interaction=nonstopmode main.tex 

#main.bbl: main.aux $(BIBFILES)
#	bibtex main

$(EXTDIR)/%.pdf: $(EXTDIR)/%.eps
	$(EPSPROG) $(EXTDIR)/$*.eps

$(SDIR)/%.pdf: $(SDIR)/%.eps
	$(EPSPROG) $(SDIR)/$*.eps

$(MDIR)/%.pdf: $(MDIR)/%.eps
	$(EPSPROG) $(MDIR)/$*.eps

clean:
	rm -v *.aux *.log *.bbl *.blg *.out *.temp *.pdf \
