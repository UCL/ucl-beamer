UCL LaTeX Beamer theme [![Build Status](https://travis-ci.com/UCL/ucl-beamer.svg?branch=master)](https://travis-ci.com/UCL/ucl-beamer)
======================

by Simon Byrne (based on the original template by Maurizio Filippone)

These files form a theme for the Beamer package in LaTeX that is a close approximation to the [UCL Corporate Identity](http://www.ucl.ac.uk/corporate-identity). 


Installation
------------

To use once, simply put the files in the directory of your document.

A more permanent solution is to put the files somewhere in your texmf tree. To find out where this is in your system, run:
```
kpsewhich -var-value TEXMFHOME
```

An appropriate place would be `<texmf>/tex/latex/uclbeamer`


Use
----

The usage of the theme and its many options are given in the file `sample.tex`. 

It can also be used for constructing a poster: a rough implementation is given in `sample-poster.tex`, however there are still some issues with spacing that need to be sorted out.


Notes
-----

By default, the package uses the Helvetica font, as Arial (the official UCL typeface) is not installed on most TeX distributions. If you really want Arial, then you should be able to get it working using the following steps:

1. Install the font using the `getnonfreefonts` script from http://www.tug.org/fonts/getnonfreefonts/.

2. You may need to run this:
```
updmap-sys --enable Map=ua1.map
```

3. Add the following lines to the preamble of your document:
```latex
\usepackage[T1]{fontenc}
\usepackage{uarial}
\renewcommand{\familydefault}{\sfdefault}
```

If you're wondering how to tell them apart, the only difference appears to be that Arial doesn't have the downstroke on the G.


Support
-------

Requires a reasonably modern TeX installation (it has only been tested on MacTeX 2012). If you're having any problems, try upgrading.

This is completely unofficial, and not supported by UCL. If you notice any bugs however, please do [open an issue](https://github.com/UCL/ucl-beamer/issues/new), or better yet, send in a pull request.

FAQ
---

## `=` and `+` are not rendered in math mode

Seen with TeXlive 2017 on macOS 10.12, reproduced on macOS 12.1, caused by deprecated [mathptmx](https://ctan.org/pkg/mathptmx?lang=en) package.

Solution: Following this [issue](https://github.com/UCL/ucl-beamer/issues/3), use [newtx](https://ctan.org/pkg/newtx) package
