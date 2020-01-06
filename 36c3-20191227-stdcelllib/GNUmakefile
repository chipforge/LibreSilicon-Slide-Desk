#   ************    LibreSilicon's StdCellLibrary   *******************
#
#   Organisation:   Chipforge
#                   Germany / European Union
#
#   Profile:        Chipforge focus on fine System-on-Chip Cores in
#                   Verilog HDL Code which are easy understandable and
#                   adjustable. For further information see
#                           www.chipforge.org
#                   there are projects from small cores up to PCBs, too.
#
#   Purpose:        Makefile for Document Generation in LaTeX
#
#   ************    GNU Make 3.80 Source Code       ****************
#
#   ////////////////////////////////////////////////////////////////
#
#   Copyright (c) 2018, 2019 by chipforge <chipforge@nospam.chipforge.org>
#   All rights reserved.
#
#       This Standard Cell Library is licensed under the Libre Silicon
#       public license; you can redistribute it and/or modify it under
#       the terms of the Libre Silicon public license as published by
#       the Libre Silicon alliance, either version 1 of the License, or
#       (at your option) any later version.
#
#       This design is distributed in the hope that it will be useful,
#       but WITHOUT ANY WARRANTY; without even the implied warranty of
#       MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
#       See the Libre Silicon Public License for more details.
#
#   ////////////////////////////////////////////////////////////////////

#   project name

TITLE =       	36c3-20191227-stdcelllib

#   directory pathes

DOCUMENTSDIR =  .
OUTPUTDIR =     ..

#   tool variables

CAT ?=          @cat
MV ?=           mv
RM ?=           rm -f
TAR ?=          tar -zh
DATE :=         $(shell date +%Y%m%d)

#   project tools

LATEX ?=        pdflatex # -output-directory $(OUTPUTDIR)

#   ----------------------------------------------------------------
#               DEFAULT TARGETS
#   ----------------------------------------------------------------

#   display help screen if no target is specified

.PHONY: help
help:
	#    -------------------------------------------------------
	#    available targets:
	#    -------------------------------------------------------
	#	
	#    help       - print this help screen
	#    clean      - clean up all intermediate files
	#
	#    talk       - compile talk
	#

.PHONY: clean
clean:
	$(RM) *.aux *.idx *.log *.toc *.out *.nav *.snm

#   ----------------------------------------------------------------
#               DOCUMENTATION TARGETS
#   ----------------------------------------------------------------

.PHONY: talk
talk:   pdf clean

.PHONY:
pdf:	$(TITLE).tex
	$(LATEX) $<
	$(MV) $(TITLE).pdf $(OUTPUTDIR)
