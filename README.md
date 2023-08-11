# Combining Stata Dyndoc with Quarto

This is an example repository of how to combine Stata [dynamic
documents](https://www.stata.com/manuals/rptdynamicdocumentsintro.pdf) with
[Quarto](https://quarto.org).

Stata documents can be named anything, but **avoid** ".md" to prevent Quarto
from overwriting them. I use ".dyndoc" here.

There is a Makefile, but the _quarto.yml document also specifies a call to the
Make as a
[pre-render](https://quarto.org/docs/projects/scripts.html#pre-and-post-render),
so clicking "Render" in RStudio should work as well. Otherwise a call to `make`
will work. In either case, Stata documents will be processed by Stata( if any
changes to them were made) to produce .qmd files, after which Quarto renders the
entire document.
