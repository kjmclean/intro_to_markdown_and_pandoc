
## The Case for Markup Languages for Typesetting

### Markup and Typesetting

*Typesetting* is the process of specifying the details of how a written document is represented visually, from the margins widths and the page size, to the font choice, style, and spacing.

In the days of the printing press, a publisher would read through a written document and add notes in the margin on how the document was to be printed. The typesetter would then follow these notes — the *Markup* — to set the physical type and generate the final printed document.

This process, *Markup* and *Typesetting*, is still how all modern day software generates written documents. While popular word processing software like *Microsoft Word* hide the mechanics from the user, underneath the hood, every bolded word and indented paragraph is specified by a *Markup language* that tells the software how to represent the document onscreen or a printer how to render it.


### WYSIWYG *vs* WYSIWYM

For most day to day purposes, word processors like *Microsoft Word* are fast and convenient. However, if you've ever written a long document (*e.g*: over 100 pages), or one with complex structure (chapters or nested subsections) or embedded images, you may have found the convenience quickly gives way to frustration and chaos.

*Microsoft Word* is what is known as a *WYSIWYG* (*What You See is What You Get*). The tradeoff for the speed and convenience of real-time typsetting is a sometimes inexplicable and often infuriating lack of control of how the document is formatted.

The alternative to the *WYSIWYG* is a *WYSIWYM* (*What You See I What You Meant*). A *WYSIWYM* usually requires the user to annotate their document as they write with a specific *Markup language*, then pass the document through some form of interpreter in order to generate the final document. While this process sacrifices the readability of real-time typsetting, and requires a certain degree of proficiency with the markup language of choice, a *WYSIWYM* (in theory) provides the user complete control over every aspect of the final document.

### Common Markup Languages

#### **html**

The most popular *Markup* language in the world is probably *html*, which is used to determine how nearly all text on the web is rendered. For a sense of how *html* markup looks, try right-clicking on this page and selecting *View Page Source*. Each one of those colons, quotes, and parentheses provides typsetting instructions for your browser. The browser then consults the page's associated *Cascading Style Sheet* (*CSS*) on how each markup instruction should be rendered onscreen. Two different *CSS* style sheets will generate two different web pages (*e.g*: different layout, text sizes, or colors).

#### \LaTeX

\LaTeX and its progenitor \TeX (pronounced "laytech" and "tech", the last letter is a Greek *Chi*, not an 'x') are part of a family of *WYSIWYM* languages originally developed for typsetting printed documents that is still widely used for typesetting books, journal articles, and theses. Like, *html*, user annotates a written document with specific markup tags then passes it through a \LaTeX interpreter that renders the final document based on the *Class* and *packages* specified by the user. While it has a steep learning curve and can be intimidating for the novice user, it is an extremely powerful tool with a large (if diminishing) user base. If you're interested in trying your hand at \LaTeX, start with our tutorial [here](https://github.com/mrsunny0/LaTeX-thesis-proposal).

#### Markdown

Markdown is the youngest and simplest of common markup languages. Variations of it are used in many websites and applications, such as *reddit*, *Wordpress*, *Slack*, and *WhatsApp*. If you've ever bolded text with a couple of asterisks, you've used *Markdown*.

