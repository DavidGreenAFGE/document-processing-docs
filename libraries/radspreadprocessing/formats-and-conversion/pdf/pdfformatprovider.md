---
title: Using PdfFormatProvider
page_title: Using PdfFormatProvider
description: Using PdfFormatProvider
slug: radspreadprocessing-formats-and-conversion-pdf-pdfformatprovider
tags: using,pdfformatprovider
published: True
position: 2
---

# Using PdfFormatProvider



__PdfFormatProvider__ is part of SpreadProcessing which allows export to PDF format.
      

## Using PdfFormatProvider

__PdfFormatProvider__ makes it easy to export a Workbook to a PDF format. Each Worksheet exported to PDF is being divided into pages according to its WorksheetPageSetup. More information about paging a Worksheet is available in the [Worksheet Page Setup]({%slug radspreadprocessing-features-worksheetpagesetup%}) documentation article.
        

## Prerequisites

In order to use __PdfFormatProvider__ you need to add references to the assemblies listed below:
        

* Telerik.Windows.Documents.Spreadsheet.dll
            

* Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.dll
            

## Export

__Example 1__ shows how to use __PdfFormatProvider__ to export a Workbook to a file.
        

#### __[C#] Example 1: PdfFormatProvider export example__

{{region cs-radspreadprocessing-formats-and-conversion-pdf-pdfformatprovider_0}}

    Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.PdfFormatProvider pdfFormatProvider = new Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.PdfFormatProvider();
    using (Stream output = File.OpenWrite("Sample.pdf"))
    {
        Workbook workbook = CreateSampleWorkbook(); // The CreateSampleWorkbook() method generates a sample spreadsheet document. Use your Workbook object here.
        pdfFormatProvider.Export(workbook, output);
    }
{{endregion}}



The result from the export method is a document that can be opened in any application that supports PDF documents.
        
#### __[C#] Example 2: Export to RadFixedDocument__
{{region cs-radspreadprocessing-formats-and-conversion-pdf-pdfformatprovider_1}}
	Workbook workbook = CreateSampleWorkbook();
	
	Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.PdfFormatProvider provider = new Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.PdfFormatProvider();
	RadFixedDocument fixedDocument = provider.ExportToFixedDocument(workbook);
{{endregion}}

>tip __RadFixedDocument__ is the base class of the __RadPdfProcessing__ library. Additional information on the library and its functionality can be found [here]({%slug radpdfprocessing-overview%}).
