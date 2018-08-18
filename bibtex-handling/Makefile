# To avoid trouble on systems where the SHELL variable might bei inherited
# from the environment. This is never a problem with GNU make, but the GNU
# make Manual recommends this setting (p. 149).
SHELL = /bin/sh

# Different make programs have incompatible suffix lists and this sometimes
# creates confusion (GNU make Manual, p. 149). The suffix list is set
# explicitly using only the suffixes needet in this Makefile.
.SUFFIXES:
.SUFFIXES: .tex .bib .eps .jpg .pdf .dvi

# Variables for the main file, includet tex files and the bib file
# BIBF: contains list of all bib files
MAIN := main
BIBF := $(wildcard *.bib)

# variables to represent external programs.
PDFLATEX := pdflatex
PDFLATEXFLAGS := -interaction=batchmode
BIBTEX := bibtex 
OPEN := open
ECHO := echo
CONVERT := convert

all: $(MAIN).pdf 

# Generate the pdf file. With a bibliograpy file (bib file), four steps are
# needet (Joachim Schlosser: Wissenschaftliche Arbeiten schreiben mit LaTeX,
# S. 170).
# 1. compile the tex file, extracting the bibliogrpahy references
# 2. solve the references with BibTeX
# 3. compilie the tex file and include the bibliography
# 4. compile the tex file and include the references 
#
# If no bib file exists, then the bibtex and consecutive pdflatex runs are not
# necessary. ToDo: not testet yet a situation when more than one bib files are
# present (e.g. in case the variable BIBF contains a list of files rather then
# one file). Maybe it will need the make function "firstword"?
$(MAIN).pdf: $(MAIN).tex  $(BIBF) 
	@$(PDFLATEX) $(PDFLATEXFLAGS) $(MAIN).tex
ifneq ("$(wildcard $(BIBF))","")
	-$(BIBTEX) $(MAIN)
	@$(PDFLATEX) $(PDFLATEXFLAGS) $(MAIN).tex
	@$(PDFLATEX) $(PDFLATEXFLAGS) $(MAIN).tex
endif
	@$(OPEN) $(MAIN).pdf


