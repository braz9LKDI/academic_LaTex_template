# Academic LaTex template

A clean, simple and customizable LaTeX template for academic reports written in Spanish.

## Features

- Structured layout: it is split into logical files for configuration, front page and main content.

- Pre-configured packages: it includes common packages for mathematics (`amsmath`, `mathtools` and `siunitx`), images (`graphicx`), algorithms (`algpseudocode`) and professional tables (`booktabs` and `multirow`).

- Polished typography: `fontenc` (T1), `lmodern` and `microtype` for proper accents (`ñ`, `á`), hyphenation and subtle typographic refinements.

- Smart references and links: `hyperref` with colored links plus `cleveref` for context-aware cross-references (`\cref{...}`).

- Custom commands: it comes with pre-defined commands for math notations like norms (`\norm`), absolute values (`\abs`) and more.

- Spanish language support: configured with `\usepackage[spanish]{babel}` and `csquotes` for proper hyphenation, quotation marks (`\enquote{...}`) and Spanish-language text elements.

## File structure

- `main.tex`: this is the **main file** you will compile. It defines the document's overall structure and includes the other parts.

- `preamble.tex`: contains all **package imports**, custom commands and page layout settings (like margins).

- `front_page.tex`: defines the **title**, **author** and **date** for the title pages.

- `assets/`: a directory where you should place your image files.

    > The template is already configured to look for images here.

## Tooling

This template is designed to be use with the [LaTeX Workshop VS Code extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), and it uses my own [`style_config`](https://github.com/braz9LKDI/style_config) kit to keep the LaTeX source consistent, specifically its `latex_simplified/` stack:

- latexindent handles formatting: indentation, line breaks around environments and alignment of tabular and math delimiters.

- chktex catches common LaTeX issues like spacing problems, bad command usage and quoting mistakes.

- latexmk orchestrates the build, running pdflatex and biber the right number of times until cross-references stabilize.

Every config in the root of this repository (`.latexindent.yaml`, `.chktexrc`, `.latexmkrc` and `.vscode/`) is a direct copy from that stack. The same setup can be adopted in any LaTeX project by copying the `latex_simplified/`.
