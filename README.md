# Computer Vision Group Siegen
This is the source code for webpage of Computer Vision group, University of Siegen.
The website is based on the template from Jon Barron's public academic website: https://jonbarron.info/, converted to Jekyll.

### Adding new publications:
To add a new publication, simply add a markdown file (*.md*) to the corresponding *_publications/&lt;YEAR&gt;* directory. The file contents must have the following format:

```
---
year: <YEAR>
month: <MONTH>
title: "<TITLE>"
award: "<AWARD_NAME>"
source: "<LINK_TO_PUBLICATION>"
authors:
  - {name: "<NAME>", link: "<LINK_TO_PROFILE_OR_NULL>"}
  - ...
publisher: "<PUBLISHER>"
image: "<PATH_TO_IMAGE>"
links:
  <NAME>: "<URL>"
  ...
---
<ABSTRACT>
```

#### Tips:
 - All fields are required, if not mentioned otherwise.
 - The title page supports markdown.
 - LaTeX-Formulas are supported in title and abstract. **Warning: Backslashes inside fomulas need to be escaped by a second backslash if used inside the title field!**
 - An `author`s `link` field can be set to `null` or left empty (note that empty means completely empty, **not** an empty string!).
 - The `image` field can be left out, in that case jekyll will automatically search for a **.png** file at *data/images/&lt;LAST_NAME_FIRST_AUTHOR&gt;&lt;PUBLISHER&gt;&lt;YEAR&gt;.png*.
 - If a field called `image2` exists, jekyll will add both images on top of each other, with a crossfading-effect when hovering over the image.
 - If no entry called *BibTeX* (case insensitive) exists in `links`, jekyll will automatically search for a **.bib** file at *data/bibtex/&lt;LAST_NAME_FIRST_AUTHOR&gt;&lt;PUBLISHER&gt;&lt;YEAR&gt;.bib*.
 - The `award` field is optional.
