   SDIR = sequence
MDIR = Figures

EPSPROG = epstopdf
FIGURES = $(MDIR)/
BIBFILES = 			

default: main.pdf
all: main.pdf 
figures: $(FIGURES)

#intermediate.temp: main.tex main.bbl
#	pdflatex -draftmode -interaction=nonstopmode main.tex >intermediate.temp
	 
%.pdf: %.tex $(FIGURES)
	pdflatex -interaction=nonstopmode $<

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
	rm -v main.pdf *.aux *.log *.bbl *.blg *.out *.temp \
