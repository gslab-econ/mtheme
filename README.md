## GSLab Metropolis

This repository houses a modified version of the [Metropolis Beamer Theme](https://github.com/matze/mtheme) from revision `2fa6084b9d34fec9d2d5470eb9a17d0bf712b6c8`.

## Instructions 
1. Clone this repo (e.g., using `git clone git@github.com:gslab-econ/mtheme`).

2. In the directory of the beamer you wish to apply `mtheme`, create a subfolder `subfolder`. (You may replace all references to `subfolder` with a name of your choosing.)

3. Copy all `.sty` files in `mtheme` to `subfolder`

4. Go to the preamble of your beamer file. For LyX beamers, click `Document`, then click `Settings`, and finally navigate to `LaTeX Preamble`.

5. Copy and paste the following lines of code to the beginning of your preamble.

   ```
   \usepackage{subfolder/beamerthememetropolis_gslab}
   \usepackage{subfolder/beamerinnerthememetropolis_gslab}
   \usepackage{subfolder/beamerouterthememetropolis_gslab}
   \usepackage{subfolder/beamercolorthememetropolis_gslab}
   \usepackage{subfolder/beamerfontthememetropolis_gslab}
   \AtEndPreamble{%
     \@ifpackageloaded{pgfplots}{%
       \RequirePackage{subfolder/pgfplotsthemetol_gslab}
     }{}
   }
   ```

   If you have changed the name of `subfolder`, remember to replace all references to `subfolder` with the name of your choosing.


## Origin

Repository is a fork of the [Metropolis Beamer Theme](https://github.com/matze/mtheme) directory from revision `2fa6084b9d34fec9d2d5470eb9a17d0bf712b6c8`.

### Steps used to obtain the `*.sty` files from the upstream `mtheme` repository

1. Open your terminal and set the current directory to the root of the `mtheme` repository.
2. Type `make sty` to the command line.
3. In root, seven `.sty` files should be created 

### Further customization done directly to output

- `.sty` files are copied and pasted to root from the above steps.
- `beamercolorthememetropolis-highcontrast.sty` is deleted.
- `.sty` files are renamed to have the `_gslab` suffix.
- `beamercolorthememetropolis_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamercolorthememetropolis}[2017/01/23 Metropolis color theme]` to `\ProvidesPackage{beamercolorthememetropolis_gslab}[2017/01/23 Metropolis color theme]`
    - Line 54: Changed from `bg=black!2` to `bg=white`
- `beamerfontthememetropolis_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamerfontthememetropolis}[2017/01/23 Metropolis font theme]` to `\ProvidesPackage{beamerfontthememetropolis_gslab}[2017/01/23 Metropolis font theme]`
- `beamerinnerthememetropolis_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamerinnerthememetropolis}[2017/01/23 Metropolis inner theme]` to `\ProvidesPackage{beamerinnerthememetropolis_gslab}[2017/01/23 Metropolis inner theme]`
    - Line 251: Commented out (which defaults line spacing to 1)
- `beamerouterthememetropolis_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamerouterthememetropolis}[2017/01/23 Metropolis outer theme]` to `\ProvidesPackage{beamerouterthememetropolis_gslab}[2017/01/23 Metropolis outer theme]`
- `beamerthememetropolis_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamerthememetropolis}` to `\ProvidesPackage{beamerthememetropolis_gslab}`
    - Line 82-90: Removed
- `pgfplotsthemetol_gslab.sty`:
    - Line 20: Changed from `\ProvidesPackage{beamer_themes/pgfplotsthemetol}` to `\ProvidesPackage{beamer_themes/pgfplotsthemetol_gslab}`

## License

The modified content in this repository is licensed under a [Creative Commons Attribution-ShareAlike4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). We inherit this license from the original Metropolis Beamer Theme. This license permits others to use, share, and modify content as long as 

  *  Appropriate credit is given to the creator.
  *  All subsequent work retains the copyright notice and is made available under the same license. 
      * "This means that if you change the theme and re-distribute it, you must retain the copyright notice header and license it under the same CC-BY-SA license. This does not affect the presentation that you create with the theme."

Also note that

  *  This content is provided "as is," without warranty of any kind, express or implied.
  *  This license does not affect the presentation that you create with the theme.

The [original creator](https://github.com/matze/mtheme) in no way endorses the content in this repository or the [GSLab organization](https://github.com/gslab-econ). 
