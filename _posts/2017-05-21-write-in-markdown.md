---
layout: post
title: How to write manuscripts in Markdown
image: /img/writing-icon-9.png
tags: [writing; skills]
---

Compared to academic writing in LaTeX, Markdown appears to be a less intimidating choice to me, considering that I have got some experences with Github README files and there is a page of "Markdown Cheat Sheet" lying in the corner of my desktop. So I was like, Hey, this is the solution to keep me focused on WRITING, not FORMATING! Hmmmmmmmm, the problem is that I am supposed to be writing this afternoon, BUT, I am now distracted to learn EVERTHING about **how to write in markdown**. Good job, me.

This [youtube video](https://www.youtube.com/watch?v=hpAJMSS8pvs&t=57s) by Nicholas Cifuentes-Goodbody was quite helpful to get me through the basics of how writing in markdown look like. So I decided to watch the rest of his video while working on one of my draft manuscript at the same time. Frankly, it was not a fluent process of learning followed by practicing, because of my limited patience and constant distractions by various fancy tools. But here is an orgainized list of resources and How-To for my own record and future reference. 

## Program - MUST HAVE
* [Pandoc](http://pandoc.org) - a powerful universal document converter
* [Marked2](http://marked2app.com) - for quick preview, convering plain text to other documents (including HTML, PDF and Word) in a wide range of styles.

## Program - OPTIONAL
* [TableFlip](http://tableflipapp.com) - edit markdown tables similiar as excel spreadsheat in place

## Q&A

### What text editor should I use to write my markdown files? 
**TextEdit** comes pre-installed in Mac OS, which opens a new document in rich text mode by default. To work in plain text mode, go to **Format > Make Plain Text** in the menu bar, or use the keyboard shortcut **Shift-Command-T**. Other coding editors like BBEdit, TextWrangler, Xcode, etc work too.

### How to make tables?
Creating tables in Markdown is straightforward, but aligning cells with tons of  `|` and `-` really sucks! **TableFlip** seems to be a useful tool but it costs $18.99... why? Marked2 was only $13.99. I will stick to this online table generator (http://www.tablesgenerator.com/markdown_tables) until I am getting really desperate. 

### How to manage reference and insert citations?
For writing with Microsoft Word, I use EndNote to organize reference and Cite-While-Your-Write. To write in plain text, I will need a `bib` (Bib(La)Tex) file, which is a plain-text document that contains metatdata for the sources of reference. To make this transition, I first exported my entire endnote library to a `bib` file, and modify 

### How do I write plain text while having a real-time preview of converted verion for checking? 
The answer is to open the plain text file with **Marked2**. But it doesn't render my `bib` citations directly, I needed to ask Marked2 to use Pandoc as a custom processer: Go to Preference, click Advanced tab, enable Preprocessor by giving the pandoc path `/usr/local/bin/pandoc` and argument `--filter pandoc-citeproc --bibliography=/Users/Jing/Dropbox/Writing/ref.bib --csl=/Users/Jing/Dropbox/Writing/style/chicago-author-date.csl`. [Here is a more detailed instruction](http://verifyandrepair.com/04-13-2016/citations-export-preview/).

### How to convert the master markdown file to ready-to-submit manuscript?
**Pandoc** is the magic tool. After installation, first type `pandoc --version` in terminal to check if installed correctly. Basic pandoc options include:

    ### Usage: pandoc <input> --bibliography <citation.bib> --smart --normalize -s -o <output>
    # --smart: prouce typographically correct output 
    # --normalize: remove repeated space, cleanning up input
    # -s: produce standalone document
    # -o: point to output file

I believe my most used conversion would be from markdown to word document. Given that pandoc's default `docx` is quite ugly, some generic style I like can be defined in a master `reference-docx`.

    pandoc manuscript.md -o manuscript.docx --bibliography=/Users/Jing/Dropbox/Writing/ref.bib --reference-docx=/Users/Jing/Dropbox/Writing/reference.docx --smart --normalize -s 

### How to prepare CV in markdown?
Same concept, CV can also be written in markdown, and converted to other formats. The simplest solution I found is [here](http://tomp.io/markdown-cv.html).



