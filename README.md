csl-citations
=============
Collection of files used to create bibliographies for manuscripts using
[Pandoc](http://johnmacfarlane.net/pandoc/). 



Files
=====
- `abbrev.json`: contains a journal abbreviation list 
- `cjfas.csl`: CSL style for the Canadian Journal of Fisheries and Aquatic
  Sciences



Usage
=====
These files can be used to create bibliographies formatted to the specific
journal using Pandoc. For example, to create a PDF from a markdown file using
the cjfas.csl style you would run:

    pandoc --csl=cjfas.csl --bibliography=refs.bib -o output.pdf input.md 

This will result in a bibliography formated like:

> Malick, M.J., Adkison, M.D., and Wertheimer, A.C. 2009. Variable effects of
>   biological and environmental processes on coho salmon marine survival in
>   southeast Alaska. Transactions of the American Fisheries Society 138:
>   846–860. doi: 10.1577/T08-177.1.

If the journal uses abbreviations for journal titles like the Canadian Journal of
Fisheries and Aquatic Sciences, you can pass the abbreviation file to Pandoc
using:

    pandoc --csl=cjfas.csl --citation-abbreviations=abbrev.json --bibliography=refs.bib input.md -o output.pdf

This will give you a bibliography formatted like this (note the abbreviated
journal title):

> Malick, M.J., Adkison, M.D., and Wertheimer, A.C. 2009. Variable effects of
>   biological and environmental processes on coho salmon marine survival in
>   southeast Alaska. Trans. Am. Fish. Soc. 138: 846–860. doi: 10.1577/T08- 177.1.



Other
=====
The cjfas.csl file was originally pulled from the [CSL
repository](https://github.com/citation-style-language/styles/blob/master/canadian-journal-of-fisheries-and-aquatic-sciences.csl)
and modified as necessary. I constructed the abbreviation list by hand and,
therefore, only contains journal titles that I have previously cited.

