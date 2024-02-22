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
