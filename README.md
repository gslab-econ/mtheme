## GSLab Metropolis

This repository houses a modified version of the [Metropolis Beamer Theme](https://github.com/matze/mtheme) from revision `7b1eed33b9076db53971586abb873cfabd88f0de`.

## Installation 

### Unix (OS X or Linux)
Assuming ssh protocol is setup to be used with GitHub, the GSLab mtheme can be installed using the following (WARNING: `sudo` is used.):

```
git clone git@github.com:gslab-econ/mtheme
sudo mkdir -p /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab
rm -f /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab/*.sty
sudo mv mtheme/*_gslab.sty /usr/local/texlive/texmf-local/tex/latex/beamer/themes/gslab
rm -rf mtheme
sudo texhash
```

### Windows (MikTeX and LyX)

1. Clone this repo (e.g. using `git clone git@github.com:gslab-econ/mtheme`).

2. Create a directory with the following structure: `your_dir/tex/latex/gslab_mtheme/`

3. Copy all `.sty` files in `mtheme` to `your_dir/tex/latex/gslab_mtheme/`

3. Open `MiKTeX Settings (Admin)` from `Start Menu`, navigate to `Roots`, click `Add`, and then add `your_dir/` to the `Roots` path. (note: only `your_dir/`, not any of the sub-directories)

4. Go to `General`, click `Refresh FNDB` and then `Update Formats`.

5. Navigate to Lyx toolbar menu `Tools`. Click `TeX Information` in the `Tools` menu and double check that `beamerthememetropolis_gslab.sty` is present in `LaTeX Styles`. If not, click `Reconfigure Lyx` in the `Tools` menu and then check again.


## Origin

Repository is a fork of the [Metropolis Beamer Theme](https://github.com/matze/mtheme) directory from revision `7b1eed33b9076db53971586abb873cfabd88f0de`.

### Steps used to obtain the *.sty files from the mtheme-master folder

1. Open Terminal and set current directory to the root of the `mtheme` directory.
2. Type `make sty` to the command line.
3. In root, there should be 6 .sty files. 

### Further customization done directly to output

- Output files are renamed to have the _gslab suffix.
- Output files are copied and pasted to root from the above steps, but 
    - beamerinnerthememetropolis_gslab.sty has a single change in line 333 where the line spacing to 1.15 instead of the default 1 is commented out.
    - beamercolorthememetropolis_gslab.sty is modified so the background color is white instead of light gray at line 53.
    - beamerthememetropolis_gslab.sty is modified so lines 83-86 replace `metropolis` with `metropolis_gslab`.


## License

The modified content in this repository is licensed under a [Creative Commons Attribution-ShareAlike4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). We inherit this license from the original Metropolis Beamer Theme. This license permits others to use, share, and modify content as long as 

  *  Appropriate credit is given to the creator.
  *  All subsequent work retains the copyright notice and is made available under the same license. 
      * "This means that if you change the theme and re-distribute it, you must retain the copyright notice header and license it under the same CC-BY-SA license. This does not affect the presentation that you create with the theme."

Also note that

  *  This content is provided "as is," without warranty of any kind, express or implied.
  *  This license does not affect the presentation that you create with the theme.

The [original creator](https://github.com/matze/mtheme) in no way endorses the content in this repository or the [GSLab organization](https://github.com/gslab-econ). 

