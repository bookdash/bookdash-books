# Book Dash books

This is a Jekyll–GitHub Pages setup for turning markdown versions of Book Dash books into HTML for web and ebooks. It's the way we create very simple ereader- and mobile-optimised HTML designed for low-cost, low-bandwidth distribution.

To get the HTML, see [the website version of these files](http://bookdash.github.io/bookdash-books/).

## Contributors

To contribute to the technical development of this markdown–Jekyll–HTML workflow, please fork and pull-request freely. Open issues here on GitHub, too.

To contribute to the books themselves, you can find the open, original files from each book's page on [the Book Dash website](http://bookdash.org).

If you're helping turn Book Dash books into HTML using our workflow, you'll need to know markdown (and specifically the [kramdown](http://kramdown.gettalong.org/) syntax) and roughly how [Jekyll](http://jekyllrb.com/) and [GitHub Pages](https://pages.github.com/) work and interact.

### Markdown tips (work in progress)

* This assumes you're using kramdown as your markdown engine.
* Poetry: You want HTML that puts each verse in a paragraph, with line breaks between lines. Add two spaces at the end of each line so that the poetry reads easily in markdown, but the HTML will have a `<br />` at the end of each line.
