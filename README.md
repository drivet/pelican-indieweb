# pelican-indieweb

A pelican theme for an IndieWeb based website.

## Pelican and IndieWeb Concepts

Pelican divides user generated content into two main types: pages and
articles.  Pages are "timeless" in the sense that they do not show up on
feeds or indexes.  Articles are time-based and show up on feeds and indexes,
usually in reverse-chronological order.

The IndieWeb community, on the other hand, tends to reserve the word
"article" for what other people would call blog entries.  Other kinds of
content on a typical IndieWeb website includes "notes" (tweet-like short
bits of text), events and photos.  All this content, in pelican, would fall
under the umbrella of "articles" since it's all time-stamped.


## Template Files

This theme is geared towards websites that are comprised of more than just a
blog, including those with potentially hundreds of standalone pages.

Pelican enforces the following mandatory templates files:

* archives.html - page for all articles in chronological order
* period_archives.html - one page for each time period defined in config
* article.html - page page for each article
* author.html - one page generated per author
* authors.html - page for all authors
* categories.html - page for all categories
* category.html - one page for each category
* index.html
* page.html - one for each page
* tag.html - one for each tag
* tags.html - page for all tags

Any other template file seen here is used for organizational purposes or
one-off pages.  For example:

### base.html

This template is the base of the entire website.  All pages ultimately
derive from this template.

### page.html

Extends base.html.  Each standalone page derives from this.

### index.html

This is the "master feed" page, which collects all the pelican articles,
notes, etc. into one long reverse-chronological list of "stuff".

### blog.html

This template is the basis of the blog subsection of the entire website.
Every page in the blog ultimately derives from the template.

Pages in the blog can directly extend this template, or can do so via the
article_list.html template.

### article_list.html

Some blog pages collect article summaries, like the tag.html template
(articles for a particular tag) or the category.html template (articles in a
particular category).  These pages derive from this template.
  




