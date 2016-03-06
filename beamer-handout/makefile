# Makefile for LaTeX file

# Usage:
# make without options: compiling beamer class in presentation mode
# make handout: compiling with class option 'handout'
#
# Constants 
# Use variables to represent external programs.
PDFLATEX := pdflatex
OPEN := open

# Constans for filenames
MAINFILE := main
HANDOUT := handout
PRAESENTATION := praes

# Constants for compile commands
COMPSTRHANDOUT := '\PassOptionsToClass{handout}{beamer} \input{$(MAINFILE)}' 
COMPSTRBEAMER := '\PassOptionsToClass{beamer}{beamer} \input{$(MAINFILE)}' 

$(PRAESENTATION).pdf: $(MAINFILE).tex
	$(PDFLATEX) -jobname $(PRAESENTATION) $(COMPSTRBEAMER)
	$(OPEN) $(PRAESENTATION).pdf

handout: $(MAINFILE).tex
	$(PDFLATEX) -jobname $(HANDOUT) $(COMPSTRHANDOUT) 
	$(OPEN) $(HANDOUT).pdf
