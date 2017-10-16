---
title: Overview
page_title: Overview
description: Overview
slug: radpdfprocessing-overview
tags: overview
published: True
position: 0
---

# Overview

__RadPdfProcessing__ is a processing library that allows creation, import and export of PDF documents.
![Rad Pdf Processing Overview 01](images/RadPdfProcessing_Overview_WPF_01.PNG)


The API of RadPdfProcessing contains two different editors, enabling you to choose between editing in a flow-like manner, or using the much more powerful and flexible fixed document structure and drawing on the page.
            
The document model of the library provides support for:

* [**Pages**]({%slug radpdfprocessing-model-radfixedpage%}): Adding, modifying or removing of pages in a document. The properties enable you to change the size of the page, its rotation and more.

* **Automatic layout**: Although the PDF format is fixed, sometimes you will need to insert the content in a way that flows on the page. RadPdfProcessing enables to achieve this easily by using  [blocks]({%slug radpdfprocessing-editing-block%}), [tables]({%slug radpdfprocessing-editing-table%}) and [lists]({%slug radpdfprocessing-editing-list%}).

* [**Images**]({%slug radpdfprocessing-model-image%}): Decoded on demand to achieve better performance. The API enables you to obtain the encoded image data. You can also control the image quality when saving the document.

* [**Geometries**]({%slug radpdfprocessing-concepts-geometry%}): Enable you to describe the geometry of a 2D shape.

* [**Form XObjects**]({%slug radpdfprocessing-model-form%}): The Form XObjects enables you to describe composite objects (consisting of text, images, vector elements, etc.) within a PDF file and reuse this content among the document, for smaller document size and better rendering performance.

* [**Interactive Forms**]({%slug radpdfprocessing-model-interactive-forms-overview%}): Create and modify PDF files containing textboxes, buttons, listboxes and other interactive controls making available for the PDF file user to interactively fill some data in the PDF document and/or digitally sign the filled document.

* [**Digital Signature**]({%slug radpdfprocessing-features-digital-signature%}): The digital signature feature enables you to sign and validate PDF document.

* [**Clipping**]({%slug radpdfprocessing-concepts-clipping%}): You can define the outline of other content elements like images and paths.

* [**Annotations**]({%slug radpdfprocessing-model-annotations-and-destinations%}): Associate an object with a location on a page of the PDF document.

* [**Destinations**]({%slug radpdfprocessing-model-annotations-and-destinations%}): Defines a particular view of a document.

* [**Colors and Color Spaces**]({%slug radpdfprocessing-concepts-colors-and-color-spaces%}): Support for different types of both.

* [**Fonts**]({%slug radpdfprocessing-concepts-fonts%}): Support for the standard PDF fonts, Type0, Type1, CIDFontType2, TrueType and more.

* [**Text and Graphic properties**]({%slug radpdfprocessing-editing-text-and-graphic-properties%}): Provide options for changing the properties of the different elements in the document elements so you can achieve a unique look.

* [**Password Protection**]({%slug radpdfprocessing-formats-and-conversion-pdf-settings%}#import-settings)

* [**Merge documents**]({%slug radpdfprocessing-model-radfixeddocument%}) and [**document pages**]({%slug radpdfprocessing-formats-and-conversion-pdf-pdfstreamwriter-pdfpagesource%}).

* [**PdfStreamWriter**]({%slug radpdfprocessing-formats-and-conversion-pdf-pdfstreamwriter-overview%}): The API exposes a functionality that provides option for exporting PDF files with unmatched performance and minimized memory footprint. Extremely useful when you need to add some content to existing document, merge or split documents.

* [**Import of PDF and export to PDF and plain text**]({%slug radpdfprocessing-formats-and-conversion-pdf-pdf%})

