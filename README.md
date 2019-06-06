Introduction
============

Sample latex for PhD dissertations.

Compiling
=========

The project uses the latexmk script to compile the latex to pdf, and a makefile
is enclosed to make compilation easier.

To generate the main pdf file, simply run the command

> make

This should, if everything is set up correctly, generate thesis.pdf

It is also possible to run latexmk in "continuous mode", such that the pdf file
is recreated every time the sources change. Continuous mode can be obtained by
running the command

> make cont

This should generate thesis.pdf and open the file using the pdf-viewer okular in Linux.
It is possible to change the pdf-viewer by changing the $pdf_previewer variable
in the configuration file "latexmkrc".

To clean up the generated files, run the command
> make clean
