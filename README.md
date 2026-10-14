# AES (Rijndael): Beamer slides

Black-and-white "terminal" Beamer deck on the Advanced Encryption Standard, with the C code beside each algorithm.

- `main.tex`, `beamerthemeterminal.sty`, `latexmkrc`: slides. The `latexmkrc` makes Overleaf compile with LuaLaTeX automatically; otherwise set Menu > Settings > Compiler to LuaLaTeX or XeLaTeX (pdfLaTeX fails)
- `main.pdf`: compiled deck
- `code/`: C implementation shown on the slides (`AES.c`, `utils.c`, `moops.c`). Note: `moops.c` here has the one-line CTR fix `xor(in_block, input)`
- `STUDY_MATERIAL.txt`: per-slide speaker notes
- `CODE_WALKTHROUGH.txt`: line-by-line explanation of the code
- `images/`: figures used in the slides

Build the C code: `gcc -c utils.c && gcc -c moops.c && gcc -o AES AES.c utils.o moops.o -lcrypto`

Theme license: see `LICENSE_theme`.
