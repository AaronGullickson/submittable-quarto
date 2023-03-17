This is a *very* early version of a [quarto](https://quarto.org) extension that is designed to assist scholars in the manuscript submission process. It comes with two custom formats.

* **submittable-pdf** - For the creation of a PDF that follows most submission practices (e.g. double-spaced, times 12 point font) and has some YAML options for making common adjustments such as endnotes.
* **submittable-docx** - Creates a word document that follows many standard conventions and serves a good starting point for any post-rendering changes that need to be made to fulfill requirements.

To install the extension:

```bash
quarto add AaronGullickson/submittable-quarto
```

To get an example template:

```bash
quarto use template AaronGullickson/submittable-quarto
```

Add the following to your YAML header to try out the formats:

```yaml
format:
  submittable-pdf:
    linestretch: 2          # line spacing (1 for single, 2 for double)
    mainfont: Times New Roman
    fontsize: 12pt          # font size (typically 10pt, 11pt, or 12pt)
    geometry: margin=1in    # controls the margin size
    papersize: letter
    colorlinks: true
    urlcolor: red
    fig-height: 3.5
    keep-tex: false
    endnotes: true
    titlepage: true
  submittable-docx:
    keep-md: false
```

The `endnotes` and `titlepage` can be turned on or off depending on needs.