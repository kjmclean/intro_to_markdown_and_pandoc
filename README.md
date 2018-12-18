## The Case for Markup Languages for Typesetting

### Markup and Typesetting

*Typesetting* is the process of specifying the details of how a written document is represented visually, from the margins widths and the page size, to the font choice, style, and spacing.

In the days of the printing press, a publisher would read through a written document and add notes in the margin on how the document was to be printed. The typesetter would then follow these notes — the *Markup* — to set the physical type and generate the final printed document.

This process: *Markup* and *Typesetting* is still how all modern day software generates written documents. While popular word processing software like *Microsoft Word* hide the mechanics from the user, underneath the hood, every bolded word and indented paragraph is specified by a *Markup language* that tells the software how to represent the document onscreen or a printer how to render it.

### WYSIWYG *vs* WYSIWYM

For most day to day purposes, word processors like *Microsoft Word* are fast and convenient. However, if you've ever written a long document (*e.g*: over 100 pages), or one with complex structure (chapters or nested subsections) or embedded images, you may have found the convenience quickly gives way to frustration and chaos.

[tweet-image](https://raw.githubusercontent.com/kjmclean/intro_to_markdown_and_pandoc/master/tweet_image.png)

*Microsoft Word* is what is known as a *WYSIWYG* (*What You See is What You Get*). The tradeoff for the speed and convenience of real-time typsetting is a sometimes inexplicable and often infuriating lack of control of how the document is formatted.

The alternative to the *WYSIWYG* is a *WYSIWYM* (*What You See I What You Want*). A *WYSIWYM* usually requires the user to annotate their document as they write with a specific *Markup language*, then pass the document through some form of interpreter in order to generate the final document. While this process sacrifices the readability of real-time typsetting, and requires a certain degree of proficiency with the markup language of choice, a *WYSIWYM* (in theory) provides the user complete control over every aspect of the final document.

### Common Markup Languages

* **html**
The most popular *Markup* language in the world is probably *html*, which is used to determine how nearly all text on the web is rendered. For a sense of how *html* markup looks, try right-clicking on this page and selecting *View Page Source*. Each one of those colons, quotes, and parentheses provides typsetting instructions for your browser. The browser then consults the page's associated *Cascading Style Sheet* (*CSS*) on how each markup instruction should be rendered onscreen. Two different *CSS* style sheets will generate two different web pages (*e.g*: different layout, text sizes, or colors).

* \LaTeX
\LaTex and its progenitor \TeX (pronounced LayTech and Tech, the last letter is a Greek *Chi*, not an 'x') are part of a family of *WYSIWYM* editors originally developed for typsetting printed documents that is still widely used for typesetting books, journal articles, and theses. Like, *html*, user annotates a written document with specific markup tags then passes it through a \LaTeX interpreter that renders the final document based on the *Class* and *packages* specified by the user. While it has a steep learning curve and can be intimidating for the novice user, it is an extremely powerful tool with a large (if diminishing) user base. If you're interested in trying your hand at \LaTeX, start with our tutorial [here](https://github.com/mrsunny0/LaTeX-thesis).

* Markdown
Markdown is the youngest and simplest of common markup languages. Variations of it are used in many websites and applications, such as *reddit*, *Wordpress*, *Slack*, and *WhatsApp*. If you've ever bolded text with a couple of asterisks, you've used *Markdown*.

## The Simplicity of Markdown

The beauty and power of Markdown lie in its simplicity. It is easy to write and easy to read.

Compare, for example, some common markup tags between *html*, \LaTeX, and their *Markdown* equivalents:

| Markup 				| html 													|
|:--------------------- | :-----------------------------------------------------|
|  Section Heading		|  \<h1 id="your-section"\>Your Section\<\/h1\> 		|
|  Subsection Heading 1	|  \<h2 id="your-section-1"\>Your Section\<\/h2\>		|
|  Subsection Heading 2	|  \<h3 id="your-section-2"\>Your Section\<\/h3\>		|
|  Bold Text			|  \<p\>\<em\>Bold\<\/em\>\<\/p\>						|
|  Italicized Text		|  \<p\>\<em\>italics\<\/em\>\<\/p\>					|
|  Bold italics 		|  \<p\>\<em\>\<em\>bold italics\<\/em\>\<\/em\>\<\/p\>	|
|  Superscripts 		|  \<p\>10\<sup\>5\<\/sup\>\<\/p\>						|
|  Subscripts 			|  \<p\>H\<sub\>2\<\/sub\>O\<\/p\>						|

	Table 1. Common html markup tags.



| Markup 				|  \LaTeX													|
|:----------------------|:---------------------------------------------------------|
|  Section Heading 1	| \\section\{Your Section\}\\label\{your-section\}			|
|  Section Heading 2	| \\subsection\{Your Section\}\\label\{your-section-1\}		|
|  Section Heading 3	| \\subsubsection\{Your Section\}\\label\{your-section-2\}	|
|  Bold Text			| \\emph\{Bold\}  											|
|  Italicized Text		| \\emph\{italics\}											|
|  Bold italics 		| \\emph\{\\emph\{bold italics\}\}							|
|  Superscripts 		| 10\\textsuperscript\{5\}									|
|  Subscripts	 		| H\\textsubscript\{2\}O									|

	Table 2. Common \LaTeX markup tags.



| Markup 				| Markdown	 		 	|
|:----------------------|:----------------------|
|  Section Heading 1	| \# Your Section		|
|  Section Heading 2	| \## Your Section		|
|  Section Heading 3	| \### Your Section 	|
|  Bold Text			| \*Bold\*				|
|  Italicized Text		| \_italics\_			|
|  Bold italics 		| \*\_bold italics\_\*	|
|  Superscripts 		| 10\^5\^				|
|  Subscripts 			| H\~2\~O				|

	Table 3. Common Markdown markup tags.

Compared to the other two, *Markdown* is much more intuitive and much less disruptive to read and write. More importantly, however, translators such as *pandoc* (see below) allow you to write in *Markdown* then convert your document. So, if you need to write text for a webpage, or want to try \LaTeX with training wheels, *Markdown* + *pandoc* is for you.
