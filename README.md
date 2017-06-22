# Tools for Academic Writing Workshop

<!-- TOC START min:1 max:3 link:true update:true -->
- [Pre-workshop: To install](#pre-workshop-to-install)
- [Discussion: Writing workflow](#discussion-writing-workflow)
  - [What's your workflow?](#whats-your-workflow)
  - [Which scenarios reveal inefficiencies in your current workflow?](#which-scenarios-reveal-inefficiencies-in-your-current-workflow)
- [Motivation: Plain-text writing workflow](#motivation-plain-text-writing-workflow)
  - [Advantages](#advantages)
- [Workshop: Plain-text writing workflow](#workshop-plain-text-writing-workflow)
  - [Overview](#overview)
  - [Write paper in Markdown](#write-paper-in-markdown)
  - [Generate output document (docx, pdf, html) using pandoc](#generate-output-document-docx-pdf-html-using-pandoc)
  - [Add inline-citations and bibliography](#add-inline-citations-and-bibliography)
  - [Specify a citation style for generated document](#specify-a-citation-style-for-generated-document)
- [Extras](#extras)
  - [Zotero browser plugins and PDF management with Zotfile](#zotero-browser-plugins-and-pdf-management-with-zotfile)
  - [Quick and dirty slides with Markdown and Marp](#quick-and-dirty-slides-with-markdown-and-marp)
  - [Plain-text outlining with Workflowy](#plain-text-outlining-with-workflowy)
  - [Revision tracking with Github Desktop](#revision-tracking-with-github-desktop)

<!-- TOC END -->



## Pre-workshop: To install

- [Zotero](https://www.zotero.org)
- [Zotero browser plugin (click icon corresponding to the internet browser you're using)](https://www.zotero.org/download/)
- Zotero plugins
  - [Zotfile](https://addons.mozilla.org/firefox/downloads/file/420697/zotfile-4.2.6-fx.xpi?src=dp-btn-primary)
  - [BetterBibTex](https://github.com/retorquere/zotero-better-bibtex/releases/download/1.6.98/zotero-better-bibtex-1.6.98.xpi)
  - [Plugin installation instructions](https://github.com/retorquere/zotero-better-bibtex/wiki/Installation)
- Pandoc: [Windows](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-windows.msi) | [Mac](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-osx.pkg)
- [Typora](https://www.typora.io/#download)
- Github Desktop: [Windows](https://github-windows.s3.amazonaws.com/GitHubSetup.exe) | [Mac](https://central.github.com/mac/latest)
- [Workflowy (Register for an online service)](https://workflowy.com/invite/eb640f.lnx)
- [Marp](https://yhatt.github.io/marp/)


## Discussion: Writing workflow

### What's your workflow?

Here's a typical workflow we follow while writing a paper:

- Reference collection
- Note-taking
- Writing and organizing paper structure
- Typesetting and layout (in format specified by target conference or publication)

What is your workflow doing the above steps? Which systems or tools do you use? Here are some possibilities:

#### Reference collection

- Look for references through Google, Google Scholar, EBSCO
- Store all PDF files in a project folder (for a specific study)
- Organize PDF files per subtopic, or paper section
- Print PDFs and organize subtopics in physical folders or envelopes
- Use a reference manager like Endnote

#### Note-taking

- Writing and highlighting on printed PDFs
- Annotating soft-copies of PDFs
- Keeping a single notebook per study and writing notes there, along with bibliographic information of source
- Copy-pasting from PDF into a Word file to collect all notes
- Collecting notes in Notepad text files

#### Writing and organizing paper structure

- Writing in Microsoft Word
- Manually adding in-text citations in citation styles of target conference or publication
- Manually generating Bibliography
- Using citation tools built into Word
- Using Endnote Word plugins to insert citations and generate bibliography

#### Typesetting and layout (in format specified by target conference or publication)

- Reformatting word document following style guide or target publication

### Which scenarios reveal inefficiencies in your current workflow?

Examples:

- In a paper-based folder system: Not being able to find a paper when you recall a certain idea but don't remember which paper it was from
- Writing in Word: Opening the file in a different computer or different version of Word breaks the formatting
- After manually adding in-text citations and bibliography: Having to change citation style for a different publication

## Motivation: Plain-text writing workflow

The goal of the workshop is to introduce a writing workflow that uses **plain text files**, authored in programs like Notepad, as opposed to **rich text files**, authored in proprietary formats like Word docx. Central to this workflow is [Markdown, which is a convention to annotate plain-text documents](http://programminghistorian.org/lessons/getting-started-with-markdown).

### Advantages

- Portable files: can be opened and edited on any computer using any program that can open text files
- Separation of content and formatting: writing in plain text removes the distraction of deciding on formatting while writing (font, line height, etc.). The goal is to get all writing done first and only then to think of layout decisions.
- Many output formats from a single source text file: [recently developed tools](http://pandoc.org) can generate many output formats (PDF, docx, odt, html) from the a single text file
- Automatic generation of inline citations and Bibliography
- No changes to source file needed when changing citation styles in output document

From [Programming Historian](http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown):

> Markdown files are stored as plain text, further adding to the flexibility of the format. Plain text files have been around since the electronic typewriter. The longevity of this standard inherently makes plain text more sustainable and stable than proprietary formats. While files produced even ten years ago in Microsoft Word and Apple’s Pages can cause significant problems when opened with the latest version, it is still possible to open a file written in any number of “dead” plain text editors from the past several decades: AlphaPlus, Perfect Writer, Text Wizard, Spellbinder, WordStar, or Isaac Asimov’s favorite SCRIPSIT 2.0, made by Radio Shack. Writing in plain text guarantees that your files will remain readable ten, fifteen, twenty years from now. In this tutorial, we outline a workflow that frees the researcher from proprietary word processing software and fragile file formats.

> It is now possible to write a wide range of documents in one format—articles, blog posts, wikis, syllabi, and recommendation letters—using the same set of tools and techniques to search, discover, backup, and distribute our materials. Your notes, blog entries, code documentation, and wikis can all be authored in Markdown. Increasingly, many platforms like WordPress, Reddit, and GitHub support Markdown authorship natively. In the long term, your research will benefit from such unified workflows, making it easier to save, search, share, and organize your materials.



## Workshop: Plain-text writing workflow

*[Adapted from Programming Historian](http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)*

### Overview

1. Write paper in Markdown
2. Generate output document (docx, pdf, html) using pandoc
3. Add in-line citations and bibliography using BibTex (aided by Zotero and BetterBibTex)
4. Specify a citation style for generated document

### Write paper in Markdown

*[Programming Historian has a good tutorial as well](http://programminghistorian.org/lessons/getting-started-with-markdown)*

1. Open Notepad in Windows, or Textedit on a Mac. Copy-paste in some text, including paragraphs and headers. Here's some *lorem ipsum* you can use:

```
Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.

Subsection 1.1

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Subsection 1.2

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Section 2

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
```



2. Save the file as `sample.md` in your Desktop. (**IMPORTANT** In Notepad: in the Save dialog, make sure to choose the file type option UTF-8. In Textedit: Before saving, click Format > Make Plain Text in the Menu bar)
3. Let's annotate our file with some Markdown! Let's start with headings. In Markdown, headings are annotated with leading `#`'s. One `#` indicates a level-1 heading, two `#`'s indicates a level-2 heading, etc. Here's our file with annotated headings.

```
# Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.

## Subsection 1.1

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

## Subsection 1.2

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

# Section 2

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
```

4. Now we have something to preview in Typora! Save your markdown file, and open your file in Typora and see how it recognizes your headings and displays them prettily.
5. Go back to Notepad and try to annotate some words or phrases as italic (surround the phrase with one asterisk: `*italic phrase*`) and bold (surround the phrase with two asterisks: `**bold phrase**`).
6. Save and switch back to Typora to preview your work so far.
7. [Try out other annotations like lists, quotes, footnotes, and tables.](http://programminghistorian.org/lessons/getting-started-with-markdown) Write in Notepad, preview in Typora.
8. Editing hint: you can actually edit your Markdown document in Typora! Click View > Source Code Mode in the Menu bar to see the raw Markdown annotations. Click that again to switch back to Preview mode.
9. Tables hint: Writing [Markdown tables](http://programminghistorian.org/lessons/getting-started-with-markdown#tables) is a pain (and takes some effort to make pretty in the source file). The easiest way I've found to create tables is this online tool: [Markdown Tables Generator](http://www.tablesgenerator.com/markdown_tables). Create your tables and copy-paste the generated Markdown into your document.

### Generate output document (docx, pdf, html) using pandoc

#### Sidebar: Command-line basics

The best way to execute pandoc at the moment is through the command line. That means you'll have to learn a tiny amount of command-line commands: `pwd` (present working directory), `ls` (list files and folders), and `cd` (change directory).

1. Fire up your command-line interface: Powershell in Windows and Terminal on a Mac.
2. Try out `pwd` and `ls` and observe the output.
3. Does the output of `ls` show names of any folder? Maybe Desktop? try `cd Desktop`.
4. Does `pwd` show a different output?
5. Try `cd ..` this command changes the directory to the parent of the current one.

#### Ok pandoc time

1. In your command line, `cd` to the directory containing your Markdown file. `ls` to ensure that you're in the right directory.
2. Input this into the command line to generate a Word document:

```
pandoc sample.md -o sample.docx
```

You can read the above like so: "Pandoc, use this markdown file to output a docx with this filename".

3. If pandoc does not output anything, the doc is ready! Go to your Desktop in your file explorer, open sample.docx, and pat yourself on the back as you admire your work.
4. Try to create an HTML file:

```
pandoc sample.md -o sample.html
```

5. How about an OpenOffice document?:

```
pandoc sample.md -o sample.odt
```
6. Are you getting the pattern? What would you change to the above command to generate a pdf? Try it now.
7. What happened? Did you get an error? This is because pandoc needs another set of tools to generate PDFs (pandoc uses LaTeX). [You'll need to install LaTeX for PDF generation to work (look for PDF output instructions).](http://pandoc.org/installing.html)
8. As an alternative, Typora can export your Markdown to PDF! Try File > Export > PDF from the Menu.

### Add inline-citations and bibliography

Pandoc works with the BibTeX format to generate inline citations and the bibliography. BibTeX is another plain-text encoding of bibliographic information. In the past, researchers wrote BibTeX files by hand, but thankfully modern reference management software can help out with generating BibTeX files.

#### Generate BibTeX file

1. In Zotero, click File > Export Library...
2. In the dialog box that appears, Choose Better BibLaTeX as the Format, and check Keep updated. Click OK.
3. Save the bib file in the same folder as your sample.md. Maybe name your bib file sample.bib
4. Open sample.bib in Notepad (or Textedit). See how the entries are formatted? Are you thankful you didn't have to write that out yourself?

#### Add citations to your source file

1. At the top of your Markdown file, add the following 3 lines. This tells pandoc where to find your bibliographic references. Your file should look like this now:

```
---
bibliography: sample.bib
---

# Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
```

2. In Zotero, right-click a library item and click Generate BibTeX key. Notice in the right sidebar how a citation key appears in the Extra box of the Bibliographic information: `hundhausen_methodology_2006`. Copy that citation key.

3. Paste the citation key as an inline citation into your markdown document like so: `[@hundhausen_methodology_2006]`. For instance.

   ```
   Writing is really awesome [@hundhausen_methodology_2006].
   ```

4. Add a final heading to the end of your document: `# Bibliography`


Here's how your document could like like when you're finished with these steps:


```
---
bibliography: sample.bib
---

# Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo [@hundhausen_methodology_2006].

# Bibliography
```


#### Generate your doc

```
pandoc main.md -o main.docx --filter pandoc-citeproc
```

Note the extra option we added at the end. View your generated document. Rejoice!



### Specify a citation style for generated document

Citation Style Language is yet another plain-text encoding, this time for specifying citation styles. [Zotero Style Repository](https://www.zotero.org/styles) is a comprehensive online database of citation styles.

1. Search for and download couple of citation styles from the [Zotero Style Repository](https://www.zotero.org/styles). Give the files short names and save them in the same folder as your sample.md. Say we downloaded APA and Chicago Manual of Style csl files and named them apa.csl and chicago.csl
2. Add another option to the top of your markdown file to specify citation style. Let's try APA first. Like this:

```
---
bibliography: sample.bib
csl: apa.csl
---

# Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo [@hundhausen_methodology_2006].

# Bibliography
```
3. With the csl files in place and your citation style specified, generate your doc again:

```
pandoc main.md -o main.docx --filter pandoc-citeproc
```
4. Open the generated doc and observe how citations and the Bibliography are formatted.
5. Now, in your Markdown file, change the citation style to Chicago:

```
---
bibliography: sample.bib
csl: chicago.csl
---

# Section 1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo [@hundhausen_methodology_2006].

# Bibliography
```
6. Repeat steps 3 and 4. See how easy that was to switch styles? All without editing any of your inline citations!

## Extras

Here are other things that either support or are enabled by this plain-text centric writing workflow. Let me know if any of these are interesting, and I'll fill in the sections with step-by-step tutorials as well.

### Zotero browser plugins and PDF management with Zotfile

### Quick and dirty slides with Markdown and Marp

### Plain-text outlining with Workflowy

### Revision tracking with Github Desktop
