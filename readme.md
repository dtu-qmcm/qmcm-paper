# QMCM paper template

[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-orange.json)](https://github.com/copier-org/copier)

This is a template that you can use for your papers.

## How to use this template

1. Install [quarto](https://quarto.org/docs/get-started/)
2. Copy this template: 

   ```sh
   copier copy gh:dtu-qmcm/qmcm-paper name-of-paper-folder --vcs-ref HEAD
   ```
3. Answer the questions.
4. `cd name-of-paper-folder`
5. Write your paper by editing the file `main.md`. 
6. Render your paper.

   ```sh
   quarto render main.md
   ```

## Handy links

[Copier documentation](https://copier.readthedocs.io/en/stable/)

## How to write your paper

Like most quarto documents, `main.md` is written in Pandoc flavour Markdown with a YAML front-matter section. See [here](https://quarto.org/docs/authoring/markdown-basics.html) for instructions on getting started with this format.

By default, the paper stores references in a BibTeX file called `bibliography.bib`. You can cite entries from that file using their citation key like so:

```
Kinetic models are great[@st.johnBayesianInferenceMetabolic2018].
```

You can generate an HTML preview of your paper by running the command `quarto preview main.md`. This will start a preview server and provide an address you can use to view your paper with your web browser. While the preview server is running, whenever you save `main.md` you should almost immediately be able to see the results in your browser.

The default output formats, which are created when you run `quarto render main.md`, are HTML, DOCX (i.e. Microsoft Word) and PDF. The PDF file is created to match the format of PLOS using [this template](https://github.com/quarto-journals/plos). If you would like to use a different template, there are a lot [here](https://quarto.org/docs/extensions/listing-journals.html). In general they are quite easy to use: just run something like:

```sh
> quarto add github-username/template-repo
```

then follow the instructions and update the `format` field of the front-matter section in `main.md`.

If you need to submit to a journal that doesn't have a quarto template yet, you can do surgery on the file `main.tex`.

Don't forget to make sure that all the authors' ORCID ids and contact details are correct.
