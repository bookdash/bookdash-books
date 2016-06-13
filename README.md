# Book Dash books

We're creating simple HTML versions of [Book Dash](http://bookdash.org) books for the web and ebooks. 

To grab the finished HTML, see [the website version of these files](http://bookdash.github.io/bookdash-books/). 

## Contributing

If you'd like to help grow and improve this collection:

*	Let us know about mistakes and problems by [logging issues here](https://github.com/bookdash/bookdash-books/issues).
*	Complete and clean up infinished versions (any [Book Dash book](http://bookdash.org/see/books) not listed [here](http://bookdash.github.io/bookdash-books/)).

Adding a book requires four components:

*	A folder in this repo, organised as `english-title/language-code`, e.g. `sleepy-mr-sloth/en` for the English edition of *Sleepy Mr Sloth*.
*	An `index.md` file in that folder (containing the story text and links to images)
*	An `images` folder in that folder (containing JPGs of the front cover and book-page images)
*	Information (metadata) about the book stored in the repo's `_config.yml` file.

For technical background on how these files are organised, see the [Electric Book Workflow](https://github.com/electricbookworks/electric-book-workflow).

### Creating the `index.md` file

Each book's `index.md` file contains all the text and links to images for the story.

This file is written in markdown: a simple way to structure plain text, which a markdown processor can turn into web- and ebook-ready HTML automatically. You can [read more about markdown here](http://electricbookworks.github.io/electric-book-workflow/guide/03-markdown.html#markdown).

The best way to learn how to create a markdown `index.md` file for a book is to look at an existing one. [Here is the raw markdown for *Sleepy Mr Sloth*](https://raw.githubusercontent.com/bookdash/bookdash-books/gh-pages/sleepy-mr-sloth/en/index.md).

It's made of four components:

1. The YAML header: the part between the three hyphens at the top of the file:

	~~~
	---
	title: Sleepy Mr Sloth
	---
	~~~

2.	The heading: `# Sleepy Mr Sloth`. In markdown, a first-level heading is indicated with a hash at the start of the line.
3. A link to each image, including a short description of what's in the image:

	~~~
	![Mr Sloth is sleepy and yawning]({{ site.image-set }}/01.jpg)
	~~~

4.	The text of the story, as plain lines of text. The image always precedes the text that relates to it. (This is because in any book we, especially children, always take in the image before we read the text on a page.)

Each of these elements must be separated by an empty line.

### Images

These digital versions include cover and story images, always saved as JPG.

* Cover images are language-specific, JPG replicas of the front covers of the book in that language. Covers must always be saved as `cover.jpg`. Cover images are always square.
* Story images do not include text, since all the text is in the story markdown/HTML. The should always be saved as two-digit numbered filenames in order: `01.jpg`, `02.jpg`, etc. The first image is the first story image in the book (i.e. not the book plate, endpapers, or title page). Story images are always landscape (a double-page-spread from the print version). There are almost always 12 story images. 

This means that story images can be reused as is for each language. Although – since each translation has its own `images` folder – we can make exceptions if necessary and use language-specific variations, should they exist and be important for the story (e.g. a text-based sign in a picture).

When preparing images, aim for 100KB per image, and about 1000 pixels across (the longest side, which should almost always be the width of the image). This makes entire books about 1.2MB in size, which is already quite large. Downstream reusers can then choose to downsample or downsize images if necessary.

The easiest way to create story images is to export to JPEG from the InDesign file, with language layers hidden. If you use this option, we recommend the following export settings:

* Export: Spreads
* Quality: Medium
* Format Method: Baseline
* Resolution (ppi): 72
* Color space: RGB
* Embed Color Profile: sRGB checked
* Anti-alias checked
* Use Document Bleed Settings: unchecked
* Simulate Overprint unchecked

### Editing the metadata file

Each book's details are included in `_data/meta.yml`.

This file is fairly easy to understand just by reading through it. Each book's details are set in two levels:

*	Info that relates to the original and, therefore, all editions of a book (e.g. the original team that created it)
	*	Info that relates to a specific translation (e.g. the language it's in).

Since even small mistakes in this file can break the whole website, only certain people are able to edit it. 

As a contributor, you can:

*	create just the lines for your book and log them as an issue, or
*	if you are familiar with GitHub, you can fork the repo, make the changes, and submit them as a pull request.

## Licence

All Book Dash content is licensed with a [Creative Commons Attribution licence](http://creativecommons.org/licenses/by/4.0/). If you contribute, you agree that your contributions carry the same license.

[![CC-BY](https://licensebuttons.net/l/by/4.0/80x15.png)](http://creativecommons.org/licenses/by/4.0/)
