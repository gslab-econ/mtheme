## Metropolis


**IMPORTANT NOTICES FOR VERSION 1.0**

* The package and theme name changed from *m* to *metropolis*!
* The `title format` values have been restructured. Please refer to the
  [manual][].

---

Metropolis is a simple, modern Beamer theme suitable for anyone to use. It tries
to minimize noise and maximize space for content; the only visual flourish it
offers is an (optional) progress bar added to each slide. The core design
principles of the theme were described in a blog post
[here](http://bloerg.net/2014/09/20/a-modern-beamer-theme.html).

Not convinced? Have a look at the [demo slides][].

![Sample](http://i.imgur.com/Bxu52fz.png)


## Installation

To install a stable version of this theme, please refer to update instructions
of your TeX distribution. Metropolis is on [CTAN][] since December
2014 thus it is part of MikTeX and will be part of TeX Live 2016.

Installing Metropolis from source, like any Beamer theme, involves four easy
steps:

1. **Download the source** with a `git clone` of the [Metropolis repository](https://github.com/matze/mtheme) or as a [zip archive](https://github.com/matze/mtheme/archive/master.zip) of the latest development version.

2. **Compile the style files** by running `make sty` inside the downloaded
    directory. (Or run LaTeX directly on `source/metropolistheme.ins`.)

3. **Move the resulting `*.sty` files** to the folder containing your
   presentation. To use Metropolis with many presentations, run `make install`
   or move the `*.sty` files to a folder in your TeX path instead (might require
   `sudo` rights).

4. **Use the theme for your presentation** by declaring `\usetheme{metropolis}` in
    the preamble of your Beamer document.


## Usage

The following code shows a minimal example of a Beamer presentation using
Metropolis.

```latex
\documentclass{beamer}
\usetheme{metropolis}           % Use metropolis theme
\title{A minimal example}
\date{\today}
\author{Matthias Vogelgesang}
\institute{Centre for Modern Beamer Themes}
\begin{document}
  \maketitle
  \section{First Section}
  \begin{frame}{First Frame}
    Hello, world!
  \end{frame}
\end{document}
```

Detailed information on using Metropolis can be found in the [manual][].

For an alternative dark color theme, please have a look at Ross Churchley's
excellent [owl](https://github.com/rchurchley/beamercolortheme-owl) theme.


## License

The theme itself is licensed under a [Creative Commons Attribution-ShareAlike
4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). This
means that if you change the theme and re-distribute it, you *must* retain the
copyright notice header and license it under the same CC-BY-SA license. This
does not affect the presentation that you create with the theme.


[demo slides]: http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/demo/demo.pdf
[manual]: http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/doc/metropolistheme.pdf
[CTAN]: http://ctan.org/pkg/beamertheme-metropolis



-------
# gslab_latex

This repository houses a modified version of the [Metropolis Beamer Theme](https://github.com/matze/mtheme).

## Installation

Assuming ssh protocol is setup to be used with GitHub, the Metropolis_gslab theme can be installed using the following (WARNING: `sudo` is used.):

```
git clone git@github.com:gslab-econ/mtheme
sudo mkdir -p /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab
rm -f /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab/*.sty
sudo mv mtheme/*_gslab.sty /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab
rm -rf mtheme
sudo texhash
```

## Origin

Repository is a fork of the [Metropolis Beamer Theme](https://github.com/matze/mtheme) directory.

### Steps used to obtain the *.sty files from the mtheme-master folder

1. Open Terminal and set current directory to root of mtheme repo.
2. Type `make sty` to the command line.
3. In root, there should be 6 .sty files. 

### Further customization done directly to output

- Files are renamed to have the _gslab suffix.
- Files in ./output is copied and pasted from the above steps, but 
    - beamerinnerthememetropolis_gslab.sty has a single change in line 333 where the line spacing to 1.15 instead of the defaul 1 is commented out.
    - beamercolorthememetropolis_gslab.sty is modified so the background color is white instead of light grey at line 53.
    - beamerthememetropolis_gslab.sty is modifed so lines 83-86 replace `metropolis` with `metropolis_gslab`.


## License

The modified content in this repository is licensed under a [Creative Commons Attribution-ShareAlike4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). We inherit this license from the original Metropolis Beamer Theme. This license permits others to use, share, and modify content as long as 

  *  Appropriate credit is given to the creator.
  *  All subsequent work retains the copyright notice and is made available under the same license. 
      * "This means that if you change the theme and re-distribute it, you must retain the copyright notice header and license it under the same CC-BY-SA license. This does not affect the presentation that you create with the theme."

Also note that

  *  This content is provided "as is," without warranty of any kind, express or implied.
  *  This license does not affect the presentation that you create with the theme.

The [original creator](https://github.com/matze/mtheme) in no way endorses the content in this repository or the [GSLab organization](https://github.com/gslab-econ). 


