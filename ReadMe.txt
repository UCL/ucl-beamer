UCL LaTeX Beamer theme

by Simon Byrne (based on the original template by Maurizio Filippone)

These files form a theme for the Beamer package in LaTeX that is a close
approximation to the UCL Corporate Identity. The usage of the theme and its
options are given in the file show.tex.


Installation
============

To use once, simply put the files in the directory of your document.

A more permanent solution is to put the files somewhere in your texmf tree. To
find out where this is in your system, type the command:

    kpsewhich -var-value TEXMFHOME

An appropriate place would be `<texmf>/tex/latex/uclbeamer`


Use
===

The usage of the theme and its many options are given in the file `show.tex`. 


Notes
=====

By default, the package uses the Helvetica font, as Arial (the official UCL
typeface) is not installed on most TeX distributions. If you really want
Arial, then I managed to get it working using the following steps:

1. Install the font using the `getnonfreefonts` script:

    http://www.tug.org/fonts/getnonfreefonts/

2. You may need to run the following line:

    updmap-sys --enable Map=ua1.map

3. Add the following lines to the preamble of your document:

    \usepackage[T1]{fontenc}
    \usepackage{uarial}
    \renewcommand{\familydefault}{\sfdefault}


If you're wondering how to tell them apart, the only difference I could
discern was that Arial doesn't have the downstroke on the G.


Support
=======

This is completely unofficial, and not supported by UCL. If you notice any
bugs however, contact simon.byrne@ucl.ac.uk, and I shall do my best to fix
them.
