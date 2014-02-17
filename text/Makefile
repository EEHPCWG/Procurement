# Makefile but currently more like a batch file
# Issue a make clean and then a make
#

TARGETS: procurement.pdf

.PHONY: all clean complete procurement

all: procurement.pdf
procurement: procurement.pdf

tex_files = $(wildcard *.tex)
bib_files = $(wildcard */*.bib)
pdf_files = $(wildcard *.pdf)

procurement.pdf: $(tex_files) $(bib_files) $(pdf_files)
	pdflatex -shell-escape procurement | tee latex.out ; \
	pdflatex -shell-escape procurement | tee latex.out; \
	pdflatex -shell-escape procurement | tee latex.out; \
	cp procurement.pdf ../downloadPDF/procurement.pdf

clean:
	find . -name '*.blg' -print | xargs rm -f; \
	find . -name '*.aux' -print | xargs rm -f; \
	find . -name '*.bbl' -print | xargs rm -f; \
	find . -name '*.log' -print | xargs rm -f; \
	find . -name '*.out' -print | xargs rm -f; \
	rm -f procurement.pdf

