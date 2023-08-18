all: set01.pdf set02.pdf set03.pdf set04.pdf set05.pdf

%.pdf: %.tex preamble.tex homework.cls
	pdflatex $<
	rm -f sets.aux
	cat *.aux > sets.aux
	cat sets.aux > $(patsubst %.tex,%.aux,$<)
	pdflatex $<
	rm -f sets.aux
