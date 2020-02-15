Introduction
============

Sample latex for PhD dissertations.

* Install TeX document production system (Latex)
To get the TeX document production system, one easy way is to download [TeX Live](https://www.tug.org/texlive/).

* Update Latex
If you already have Latex (Tex Live) in your machine,
then it to the latest version first.

Compiling
=========

The project uses the latexmk script to compile the latex to pdf, and a makefile
is enclosed to make compilation easier.

* To generate the main pdf file, simply run the command

`> make`

This should, if everything is set up correctly, generate thesis.pdf

* It is also possible to run latexmk in "continuous mode", such that the pdf file
is recreated every time the sources change. Continuous mode can be obtained by
running the command

`> make cont`

This should generate thesis.pdf and open the file using the pdf-viewer okular in Linux.
It is possible to change the pdf-viewer by changing the $pdf_previewer variable
in the configuration file "latexmkrc".

* To clean up the generated files, run the command

`> make clean`

* Other possible ways to use Latex and compile

1. [TeXstudio](https://www.texstudio.org/)

2. [Using Atom as a LaTeX editor](https://medium.com/@lucasrebscher/using-atom-as-a-latex-editor-93756de3d726)

3. vim/nvim
  a. [Install NeoVim and Plugins with vim-plug](https://www.linode.com/docs/tools-reference/tools/how-to-install-neovim-and-plugins-with-vim-plug/)
  
  b. [Setup Neovim for Latex](https://yufanlu.net/2018/09/03/neovim-latex/)
  
  c. [Awesome vim plugins for writers](https://opensource.com/article/17/2/vim-plugins-writers)
  
  d. [10 Vim Plugins for Writing](https://dev.to/tomfern/10-vim-plugins-for-writing-2k66)
