---
title: Settings
page_title: Settings
description: Settings
slug: radpdfprocessing-formats-and-conversion-pdf-settings
tags: settings
published: True
position: 3
---

# Settings



__PdfFormatProvider__ provides you with the ability to import/export PDF documents. Additionally, you can take advantage of the import/export settings that give you modification options.
      

## Import Settings

You can specify the import settings you wish through the __ImportSettings__ property of __PdfFormatProvider__.The available import settings are listed below:

__UserPasswordNeeded__

The event is fired when a user password is needed to open the document. The password can be specified in the __PasswordNeededEventArgs.Password__ property.
        

__Example 1__ shows how you can create a __PdfImportSettings__ object and assign it to a PdfFormatProvider.
        

#### __[C#] Example 1: Import settings__

{{region cs-radpdfprocessing-formats-and-conversion-pdf-settings_0}}
	PdfFormatProvider provider = new PdfFormatProvider();
	PdfImportSettings settings = new PdfImportSettings();
	settings.UserPasswordNeeded += (s, a) =>
	{
	    a.Password = "D0cum3ntP4ssw0rd";
	};
	
	provider.ImportSettings = settings;
{{endregion}}



## Export Settings

In order to modify the way content is exported, you can set the __ExportSettings__ property of __PdfFormatProvider__. These are the modification options you can use:
        

__IsEncrypted__

This property specifies if the document should be encrypted. The default value is *False*. The encryption algorithm used when exporting encrypted documents is **RC4**.

>This setting is ignored when __ComplianceLevel__ differs from __None__ as PDF/A compliant documents do not allow encryption.

__UserPassword__

The password to be used if the document is encrypted. The default password is an empty string.

__ImageQuality__

The **ImageQuality** property specifies the quality with which images are exported to PDF. More information about how it works is available in [this article]({%slug radpdfprocessing-concepts-imagequality%}).

>note .NET Standard specification does not define APIs for converting images or scaling their quality. Thats why, to allow the library to export images different than Jpeg and Jpeg2000 or ImageQuality different than High, you will need to provide an implementation of the **JpegImageConverterBase** abstract class and set this implementation to the **JpegImageConverter** property of the of **FixedExtensibilityManager**. For more information check the [Cross-Platform Support]({%slug radpdfprocessing-cross-platform%}) help article.

__ComplianceLevel__

Specifies the PDF/A compliance level. It can have one of the following values: 

* __None__: Specify no compliance level.
* __PdfA1B__: Specify PDF/A-1b compliance level.
* __PdfA2B__: Specify PDF/A-2b compliance level.
* __PdfA2U__: Specify PDF/A-2u compliance level.
* __PdfA3B__: Specify PDF/A-3b compliance level.
* __PdfA3U__: Specify PDF/A-3u compliance level.

The default value is __None__. For more information on PDF/A compliance, check the [PDF/A Compliance article]({%slug radpdfprocessing-howto-comply-with-pdfa-standard%}).

__Example 2__ shows how you can create a __PdfExportSettings__ object and assign it to a PdfFormatProvider.
        

#### __[C#] Example 2: Export settings__

{{region cs-radpdfprocessing-formats-and-conversion-pdf-settings_1}}
	PdfFormatProvider provider = new PdfFormatProvider();
	PdfExportSettings settings = new PdfExportSettings();
	settings.IsEncrypted = true;
	settings.UserPassword = "D0cum3ntP4ssw0rd";
	settings.ImageQuality = ImageQuality.Medium;
	settings.ComplianceLevel = PdfComplianceLevel.PdfA2B;
	
	provider.ExportSettings = settings;
{{endregion}}


## See Also

* [PdfExportSettings API Reference](https://docs.telerik.com/devtools/document-processing/api/Telerik.Windows.Documents.Fixed.FormatProviders.Pdf.Export.PdfExportSettings.html)
* [How to Comply with PDF/A Standard]({%slug radpdfprocessing-howto-comply-with-pdfa-standard%})
