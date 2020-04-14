#!/usr/bin/make -f
default:
	latexmk -pdf thesis.tex
	open -a Preview thesis.pdf 
cont:
	latexmk -pdf -pvc -view=pdf thesis.tex
	open -a Preview thesis.pdf 
clean:
	@latexmk -C
	@rm -f *.brf
	@rm -f *.lol
	@rm -f *.out
	@rm -f *.bbl
	@rm -f *.blg
	@rm -f *.upa
	@find . -name \*.aux -delete
