TEX      = xelatex
BIB      = bibtex
MAIN     = report

target: close wipe clean tex clean open

tex: $(MAIN).tex
	$(TEX) $<
	$(BIB) $(MAIN)
	$(TEX) $<
	$(TEX) $<

nobib: $(MAIN).tex
	$(TEX) $<
	$(TEX) $<

open: $(MAIN).pdf
	cmd /c start $(MAIN).pdf

close:
	cmd /c taskkill /im Acrobat.exe /t /f || echo not find

clean:
	del /s /f *.aux *.bbl *.blg *.log *.out *.gz *.toc *.thm *.fdb_latexmk *.fls *.nav *.snm *.vrb *-blx.bib *.xml

wipe:
	del /f $(MAIN).pdf

.PHONY: open close clean wipe
