NAME := RealAnalysis
WORKBOOK := RealAnalysisWorkBook
LATEXMK := latexmk
LATEXMKFLAGS := -pdf

ifeq ($(OS),Windows_NT)
    # Windows specific commands
    FIND_CMD = cmd /c 'dir /b /s'
    RM_CMD = cmd /c 'del'
else
    # Linux/Unix commands
    FIND_CMD = find . -name
    RM_CMD = rm -f
endif

TEX = $(shell $(FIND_CMD) '*.tex')
BIB = $(shell $(FIND_CMD) '*.bib')
STY = $(shell $(FIND_CMD) '*.sty')
CLS = $(shell $(FIND_CMD) '*.cls')
FIGS = $(shell $(FIND_CMD) '*.png' -o -name '*.jpg')

all:${NAME}.pdf ${WORKBOOK}.pdf

${NAME}.pdf:$(TEX) $(BIB) $(STY) $(CLS) $(FIGS)
	$(LATEXMK) $(LATEXMKFLAGS) $(NAME)
	$(LATEXMK) $(LATEXMKFLAGS) $(WORKBOOK)
#	${MAKE} clean

clean:
	$(LATEXMK) -c $(NAME)
	$(LATEXMK) -c $(WORKBOOK)
	$(RM_CMD) *.bbl *.thm *.xml *.out.ps *.dvi *.rel *.spl

purge:
	$(LATEXMK) -C $(NAME)
	$(LATEXMK) -C $(WORKBOOK)
	$(RM_CMD) -r *.bbl *.thm *.xml *.out.ps *.dvi *.rel *.spl *.pdf
	$(RM_CMD) ./tikz/*.aux ./tikz/*.log ./tikz/*.pdf ./tikz/*.gz

.PHONY: all clean purge