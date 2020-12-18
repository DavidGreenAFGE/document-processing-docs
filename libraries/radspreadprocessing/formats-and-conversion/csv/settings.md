---
title: Settings
page_title: Settings
description: Settings
slug: radspreadprocessing-formats-and-conversion-csv-settings
tags: settings
published: True
position: 2
---

# Settings



__CsvFormatProvider__ allows to import and export CSV documents. Additionally, there are a number of settings that allow you to modify the import/export. The current article outlines the available settings.
      

## 

__CsvFormatProvider__ exposes a __Settings__ property of type __CsvSettings__. This allows you to specify the following:
        

* __Delimiter__: Gets or sets the list separator. By default the CsvFormatProvider class imports and exports files using the list separator specified by the current culture of the system.
            

* __Quote__: Gets or sets the quote symbol.
            

* __HasHeaderRow__: Specifies whether the document has a header row. The default value is __false__.
            

* __Encoding__: Gets or sets the character encoding that is used when importing or exporting a file. The default value is UTF8 with BOM.
            

__Example 1__ shows how to create and specify a particular setting to a CsvFormatProvider.
        

#### __[C#] Example 1: Use CsvSettings__

{{region cs-radspreadprocessing-formats-and-conversion-csv-settings_0}}
	CsvFormatProvider provider = new CsvFormatProvider();
	provider.Settings.Delimiter = ';';
	provider.Settings.Quote = '^';
	provider.Settings.HasHeaderRow = true;
	provider.Settings.Encoding = new UTF8Encoding();
{{endregion}}


