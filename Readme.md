# LPiL Magic Runner

This is a very simple and highly specific tool to:

1. read the TeX-Magic comments in a TeX file to determine:
   - which program { lualatex or metafun(context) } to use
   - which preamble to (pre) load
   - which postamble to (post) load

2. if needed, re-run the command until the associated "check" file has
   "stabilized" (this technique has been inspired by
   [texcaller](https://github.com/vog/texcaller)
   see: texcaller/c/texcaller.c
   and search for 'run command as often as necessary')

## Dependencies

At the moment, `lpilMagicRunner` assumes that the following tools have
been installed:

1. `lualatex` which is used to typeset our LPiL based LaTeX. `lualatex`
   can be installed using [TeX Live - TeX Users
   Group](https://tug.org/texlive/)

2. 'context' which is used to typeset Metafun based diagrams. `context`
   can be installed from [Context Garden](https://contextgarden.net)

3. `cmScan` which is used to scan for our references from our NikolaBase
   citation system. `cmScan` can be installed from
   [litProgLaTeX/citationManager-tools](https://github.com/litProgLaTeX/citationManager-tools)

4. `lpilPygmentize` which is used to colourise all source code (including
   metafun diagram sources) included in any documents. `lpilPygmentize`
   can be installed from
   [litProgLaTeX/lpil-pygmentizer](https://github.com/litProgLaTeX/lpil-pygmentizer)

In addition:

- typesetting of LPiL based LaTeX (using `lualatex`) requires
  the LPiL LaTeX macros provided by the
  [litProgLaTeX/lpil-latex](https://github.com/litProgLaTeX/lpil-latex)
  project.

- typesetting the MetaFun based diargarms (using `context`) requires the
  LPiL Metafun macros provided by the
  [litProgLaTeX/lpil-context](https://github.com/litProgLaTeX/lpil-context)
  project.

