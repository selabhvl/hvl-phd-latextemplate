Introduction
============

Latex template for HVL PhD dissertations.

The template uses the latexmk to compile the latex to pdf by running a makefile enclosed.

All the default settings of the template are in the preamble.tex and macros.tex.

The default language is the American language. 

If you want to change the language, then you need to check the option of the [babel](https://ctan.org/pkg/babel?lang=en) package.

The font size of the PhD thesis template is 12pt.

The fonts used in the template include:
1. [Palatino](https://en.wikipedia.org/wiki/Palatino#Palatino) font with old-style figures: [newpxtext](https://ctan.org/pkg/newpx?lang=en) package.

If you do not want to use old-style figures, then you can change to [tgpagella](https://tug.org/FontCatalogue/texgyrepagella/) package.

2. Typewriter font: [beramono](https://tug.org/FontCatalogue/beramono/) package.

3. The Euler-VM fonts for maths (blend well with Palatino): [eulervm](http://ftp.riken.jp/tex-archive/fonts/eulervm/doc/latex/eulervm/eulervm.pdf) package. 

Part 2 of the PhD latex template consists of a collection of publications via including
a papers.tex file. If you want to write the thesis in monograph style, then you
don't need to include papers.tex.

For the thesis by publications style, in the papers.tex file, the default
setting is to use ``` \includepdf{} ``` to include PDF files in the papers folder.
The reason to choose this way to directly attach PDF files is to make the life
easier.

But, if you don't like this way, you can use ``` \subimport{} ``` instead of 
``` \includepdf{} ``` in papers.tex to compile all your latex files from your pervious publications.

However, the [HVL PhD thesis Word template](https://www.hvl.no/contentassets/14ac5045c88248ffa1cf8c4927111040/hvl-avhandling.dotx/) (page 11) on the HVL website states: 


    "Publiserte artikler kan settes inn i avhandlingen slik de er publiserte og trenger ikke konverteres til denne malen."


So, if you want to directly attach original publications (with original publishers' format pdf files), 
you only need to use "includepdf", but you might need to check the copyright of your publications about republishing.
However, if you don't want to attach pdf files directly but prefer to recompile 
your Latex files for previous papers, then just can use "subimport".   
You can ask doctoral adviser Prof. Håvard Helstrup and your supervisors to get 
their opinions for which way is reasonable and how to deal with copyright of your publications.

Latex books in case you need:
1. [LaTeX for Complete Novices](https://www.dickimaw-books.com/latex/novices/index.html)

2. [Using LaTeX to Write a PhD Thesis](https://www.dickimaw-books.com/booklist.php?book_id=18)

Install/Upate Latest Latex
========
* Install TeX document production system (Latex):

To get the TeX document production system, one easy way is to download [TeX Live](https://www.tug.org/texlive/).

* Update Latex:

If you already have Latex (Tex Live) in your machine, then update it to the latest version first.

Compiling
=========

* To generate the main pdf file, you can simply run the command defined in the
  Makefile:

`> make`

This should generate the thesis.pdf if everything is set up correctly, 

* To run latexmk in "continuous mode" such that the thesis.pdf file
is recreated every time the sources change after saving. 
The continuous mode can be executed by running the command:

`> make cont`

Both should generate thesis.pdf and open the file using the pdf-viewer.
The default setting in the Makefile is to use Preview to open thesis.pdf in
MacOS.
If, e.g., in Linux, you need to change the Makefile for the pdf-viewer you want
to use, such as [okular](https://okular.kde.org/): `okular thesis.pdf`.

* To clean up the generated files, you can run the command

`> make clean`


NOTE: if you do NOT want to use the Makefile, then compile in following 4 steps:

1. `pdflatex thesis.tex`

2. `bibtex thesis`

3. `pdflatex thesis.tex`

4. `pdflatex thesis.tex`

Possible ways to use Latex: 
=========

1. vim/[neovim](https://neovim.io/), definitely can speed up the writing process by autocomplete, snippet, etc. plugins 

      a. [Install NeoVim and Plugins with vim-plug](https://www.linode.com/docs/tools-reference/tools/how-to-install-neovim-and-plugins-with-vim-plug/)
  
      b. [Setup Neovim for Latex](https://yufanlu.net/2018/09/03/neovim-latex/)

      c. [Intelligent autocompletion Coc](https://github.com/neoclide/coc.nvim)

      d. [Semantic completion support: tabnine](https://github.com/neoclide/coc-tabnine)
  
      e. [Awesome vim plugins for writers](https://opensource.com/article/17/2/vim-plugins-writers)
  
      f. [10 Vim Plugins for Writing](https://dev.to/tomfern/10-vim-plugins-for-writing-2k66)

      g. To speed up the wirting if there are lots of mathematics: [take notes in mathematics lectures using LaTeX and Vim](https://castel.dev/post/lecture-notes-1/)

2. [Emacs](https://www.gnu.org/software/emacs/). Although I used neovim to finish my thesis, one colleague and friend of me seems used Emacs to write his thesis. I guess some one knows about the Editor war, so I also put Emacs here.;)

3. [Using Atom as a LaTeX editor](https://medium.com/@lucasrebscher/using-atom-as-a-latex-editor-93756de3d726)

4. [Overleaf](https://www.overleaf.com/)

5. [TeXstudio](https://www.texstudio.org/)
