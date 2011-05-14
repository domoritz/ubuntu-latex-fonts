This project enables you to use the original Ubuntu Font Familiy (see: http://font.ubuntu.com/) with LaTeX2e.

Currently available fonts are Ubuntu regular, Ubuntu italic, Ubuntu bold and Ubuntu bold italic and can be changed by using the common <code>\\textit</code>, <code>\\textbf</code> commands.

##How to install##

You can just drop all these files into your project and start using the fonts.

For global usage you will have to copy them into their according directories in your LaTeX-Distribution, e.g. for the Font Metrics on Texlive:

	mkdir -p /usr/share/texmf-texlive/fonts/tfm/public/ubuntu/
	cp *.tfm /usr/share/texmf-texlive/fonts/tfm/public/ubuntu/
	texhash /usr/share/texmf-texlive/

##How to use##

If you want to change your font set mid-in your document just write:

	\usefont{T1}{ubuntu}{m}{n}

In case you'd liked to have you entire document be set using this font family add this to your preamble:

	\usepackage{ubuntu}

##What is missing##

The fonts were converted as described by Gordon Grubert (http://fachschaft.physik.uni-greifswald.de/~stitch/ttf.html). However they are just bitmaps by now, what definitly has to be changed.

And of course an automated installation (i.e. a nice Makefile) is missing yet.

