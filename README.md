# PyMuPDF 1.13.19

![logo](https://github.com/rk700/PyMuPDF/blob/master/demo/pymupdf.jpg)

Release date: September 1, 2018

**Travis-CI:** [![Build Status](https://travis-ci.org/rk700/PyMuPDF.svg?branch=master)](https://travis-ci.org/rk700/PyMuPDF)

On **[PyPI](https://pypi.org/project/PyMuPDF)** since August 2016: [![](https://pepy.tech/badge/pymupdf)](https://pepy.tech/project/pymupdf)

# Authors
* [Ruikai Liu](mailto:lrk700@gmail.com)
* [Jorj X. McKie](mailto:jorj.x.mckie@outlook.de)

# Introduction

This is **version 1.13.19 of PyMuPDF (formerly python-fitz)**, a Python binding with support for [MuPDF 1.13.0](http://mupdf.com/) - "a lightweight PDF, XPS, and E-book viewer".

MuPDF can access files in PDF, XPS, OpenXPS, CBZ, EPUB and FB2 (e-books) formats, and it is known for its top performance and high rendering quality.

With PyMuPDF you therefore can access files with extensions like ".pdf", ".xps", ".oxps", ".cbz", ".fb2" or ".epub" from your Python scripts.

See the [Wiki](https://github.com/rk700/PyMuPDF/wiki) for more information, [news](https://github.com/rk700/PyMuPDF/wiki/Change-and-News-Log), release notes and usage recipes.

# Installation

For all **Windows** and (thanks to our user **@jbarlow83**!) for the major **Mac OSX** and **Linux** versions we offer [wheels](https://github.com/rk700/PyMuPDF/releases/latest). They can also be found in the [download section of PyPI](https://pypi.org/project/PyMuPDF/#files).

The platform tag for Mac OSX is `macosx_10_6_intel`.

The platform tag for Linux is `manylinux1_x86_64`, which makes these wheels usable on Debian, Ubuntu and most other variations.

On other operating systems you need to generate PyMuPDF yourself. Before you can do this, you must download and generate MuPDF. This process depends very much on your system. For most platforms, the MuPDF source contains prepared procedures for achieving this.

Be sure to download the official MuPDF source release from [here](https://mupdf.com/downloads). Do **not use** MuPDF's [GitHub repo](https://github.com/ArtifexSoftware/mupdf). It contains their current **development source**, which is **not compatible** with the published PyMuPDF version most of the time.

Once this is done, adjust directories in ``setup.py`` and the rest should be as easy as running the usual ``python setup.py install``.

The following sections contain some platform-specific comments.

## Ubuntu
One of our users (thanks to **@gileadslostson**!) has documented his MuPDF installation experience from sources in this [Wiki page](https://github.com/rk700/PyMuPDF/wiki/Experience-from-an-Ubuntu-installation).

## OSX
First, install the MuPDF headers and libraries, which are provided by mupdf-tools: ``brew install mupdf-tools``.

Then you might need to ``export ARCHFLAGS='-arch x86_64'``, since ``libmupdf.a`` is for x86_64 only.

Finally, please double check ``setup.py`` before building. Update ``include_dirs`` and ``library_dirs`` if necessary.

## MS Windows

In addition to wheels, this platform offers [pre-generated binaries](https://github.com/JorjMcKie/PyMuPDF-Optional-Material) in a ZIP format, which can be used without PIP.

If you are looking to make your own binary, consult this [Wiki page](https://github.com/rk700/PyMuPDF/wiki/Windows-Binaries-Generation). It explains how to use Visual Studio for generating MuPDF in quite some detail.

# Usage and Documentation
For all document types you can render pages in raster (PNG) or vector (SVG) formats, extract text and access meta information, links, annotations and bookmarks, as well as decrypt the document. For PDF files, most of these objects can also be created, modified or deleted. Plus you can rotate, re-arrange, duplicate, create, or delete pages and join or split documents.

Specifically for PDF files, PyMuPDF provides update access to low-level structure data, supports handling of embedded files and modification of page contents (like inserting images, fonts, text, annotations and drawings).

Other features include embedding vector images (SVG, PDF) such as logos or watermarks, "posterizing" a PDF or creating "booklet" and "4-up" versions.

You can now also create PDF Form fields with support for text, checkbox, listbox and combobox widgets.

Have a look at the basic [demos](https://github.com/rk700/PyMuPDF/tree/master/demo), the [examples](https://github.com/rk700/PyMuPDF/tree/master/examples) (which contain complete, working programs), and the **recipes** section of our [Wiki](https://github.com/rk700/PyMuPDF/wiki) sidebar, which contains more than a dozen of guides in How-To-style.

Our documentation, written using Sphinx, is available in various formats from the following sources.

* You can view it online at [Read the Docs](https://pymupdf.readthedocs.io/). For **best quality downloads** use the following links.
* zipped [HTML](https://github.com/rk700/PyMuPDF/tree/master/doc/html.zip)
* [Windows CHM](https://github.com/JorjMcKie/PyMuPDF-optional-material/tree/master/doc/PyMuPDF.chm)
* [PDF](https://github.com/rk700/PyMuPDF/tree/master/doc/pymupdf.pdf)

# Earlier Versions
Earlier versions are available in the [releases](https://github.com/rk700/PyMuPDF/releases) directory.

# License
PyMuPDF is distributed under GNU GPL V3. Because you will implicitely also be using MuPDF, its license GNU AFFERO GPL V3 applies as well. Copies of both are included in this repository.

# Contact

Please submit questions, comments or issues [here](https://github.com/rk700/PyMuPDF/issues), or directly contact the authors via their e-mail addresses.
