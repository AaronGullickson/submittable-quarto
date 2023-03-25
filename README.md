This is a [Quarto](https://quarto.org) extension that is designed to assist scholars in the manuscript submission process. It comes with two custom formats.

* **submittable-pdf** - For the creation of a PDF that follows most submission practices (e.g. double-spaced, times 12 point font) and has some YAML options for making common adjustments such as endnotes. You can see a preview of the template at <https://aarongullickson.quarto.pub/demo-of-the-submittable-format/>
* **submittable-docx** - Creates a word document that follows many standard conventions and serves a good starting point for any post-rendering changes that need to be made to fulfill requirements.

These formats are not designed to be pretty formats but rather formats that will conform or can easily be made to conform with journal submission standards. If you want a pretty format, I suggest taking a look at my [custom aog-article template](https://github.com/AaronGullickson/aog-article-quarto).

## Installation

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
    keep-tex: false
    endnotes: true
    titlepage: true
  submittable-docx:
    keep-md: false
```

## Customization

The `submittable-pdf` format currently comes with two additional yaml arguments for customization:

* `endnotes`: When set to true, footnotes will be moved to endnotes at the end of the document.
* `titlepage`: When set to true, a separate title page with author information will be printed on the first page. When set to false, the manuscript will be anonymous.

Additionally, because the template only modifies partials, all of the normal customization available to the PDF format is accessible here. Here are the defaults set in the template, which the user may modify in the yaml:

```yaml
pdf:
  documentclass: article
  linestretch: 2          # line spacing (1 for single, 2 for double)
  mainfont: Times New Roman
  fontsize: 12pt          # font size (typically 10pt, 11pt, or 12pt)
  geometry: margin=1in    # controls the margin size
  papersize: letter
  colorlinks: true
  urlcolor: red
  fig-height: 4
  fig-width: 7.5
```
