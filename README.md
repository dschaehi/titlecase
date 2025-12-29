# titlecase

Automatic title case formatting for LaTeX titles and sectioning commands.

## Features
- Provides a `\titlecase{...}` command for manual use.
- Optional automatic title-casing for `\title` and common sectioning commands.
- Lowercases common short words (per `mfirstuc` rules).
- Capitalizes each part of hyphenated words (e.g., `vision-language` -> `Vision-Language`).

## Installation
- Place `titlecase.sty` next to your `.tex` file, or
- Install into your local texmf tree (for example, `~/texmf/tex/latex/titlecase/`) and run `mktexlsr` if your TeX distribution requires it.

## Usage
```tex
\usepackage[title,section]{titlecase}

\title{an example of title case in latex}
\section{vision-language models in the wild}

\begin{document}
\maketitle
\end{document}
```

Apply to all standard sectioning commands and `\title`:
```tex
\usepackage[all]{titlecase}
```

Manual use anywhere:
```tex
\titlecase{an on-the-fly example for the title}
```

## Options
- `title`
- `section`
- `subsection`
- `subsubsection`
- `paragraph`
- `subparagraph`
- `all` (enables `title` and all standard sectioning commands)

If you omit options, no automatic redefinition happens; only `\titlecase{...}` is provided.

## Default "small words" list
The package adds the following words to the non-capitalization list:

```
a, an, the, and, but, or, nor, for, so, yet,
as, at, by, from, in, of, on, to, with, via, per, without
```

To add more words, call `\MFUnocap{<word>}` after loading the package.

## Requirements
- `mfirstuc`
- `xparse`
- `letltxmacro`

## License
MIT. See `LICENSE`.
