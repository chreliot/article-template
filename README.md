# article-template

This is my template for new articles. 

## What's in the template's main .tex file

 1. [`biblatex-chicago` package](https://ctan.org/pkg/biblatex-chicago?lang=en) package for citations, configured to my preferences.
 2. [`nameauth` package](https://ctan.org/pkg/nameauth) for smart usage of names. Example: `\cd\ wrote a book expressing \cd's ideas.` becomes ”Charles Darwin wrote a book expressing Darwin's ideas.”
 3. [`csquotes` package]
 4. [`hyperref` package] `hypersetup` for including PDF metadata.
 5. [`fontspec` package] for Unicode/UTF-8 input and processing with LuaTeX.

## What else is in this repo


## Cloning this template to use locally

This is a GitHub [template repo](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template), so we can clone it, change the name to the name of our project, and get writing. Using the nice [github command-line tool](https://cli.github.com), we can clone it with:
```
gh repo create <localname> -c --private --template article-template 
```
(Or, instead of `--template`  you can use `-p`.)

Example:
```
gh repo create darwin-project -c --private -p article-template
```
Here, the `-c` option clones it locally. And you can use `--public` instead of `--private` if you like. 

## Output to HTML or ODT

We can typeset to an HTML file using `make4ht -lue mybuild.mk4 article.tex`  (tested 2025-04-23). The command line options used here from [the make4ht documentation Section 2.1](https://www.kodymirus.cz/make4ht/make4ht-doc.html#command-line-options) are:

* **-u**,--utf8  For output documents in utf8 encoding
* **-e**,--build-file (default nil)  If the build filename is different than `filename`.mk4
* **-l**,--lua  Use lualatex for document compilation

The `mybuild.mk4` file is verbatim from [this StackExchange answer](https://tex.stackexchange.com/a/360019) by Michal Hoftich.