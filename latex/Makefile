#!/usr/bin/make -f
default:
	latexmk -pdf thesis.tex

cont:
	latexmk -pdf -pvc -view=pdf thesis.tex

clean:
	@latexmk -C
	@rm -f *.brf
	@rm -f *.lol
	@rm -f *.out
	@rm -f *.bbl
	@rm -f *.blg
	@find . -name \*.aux -type f -delete
