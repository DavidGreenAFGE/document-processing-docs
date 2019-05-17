---
title: Add, Remove and Reorder Worksheets
page_title: Add, Remove and Reorder Worksheets
description: Add, Remove and Reorder Worksheets
slug: radspreadprocessing-working-with-worksheets-add-remove-worksheets
tags: add,and,remove,worksheets, move, reorder
published: True
position: 1
---

# Add, Remove and Reorder Worksheets



This article demonstrates how to add, remove and reorder worksheets inside a workbook.
      
## Add Worksheets

Adding a new worksheet to a workbook can be easily achieved through its __Worksheets__ collection. The collection exposes an __Add()__ method that does not take arguments and returns the instance of the newly created worksheet. By default worksheets are assigned the first available name in the sequence Sheet1, Sheet2, Sheet3… You can easily change the name of the worksheet through the __Worksheet.Name__ property. More information about renaming a worksheet is available in the [Rename a Worksheet]({%slug radspreadprocessing-working-with-worksheets-rename-worksheet%}) article.
        

__Example 1__ creates a workbook from scratch and adds a single worksheet to it. Since this is the first worksheet in the workbook, it is also set as the active worksheet. All worksheets added after it will not become active.
        

#### __[C#] Example 1: Create a workbook and add a worksheet to it__

{{region cs-radspreadprocessing-working-with-worksheets-add-remove-worksheets_0}}
	Workbook workbook = new Workbook();
	Worksheet newWorksheet = workbook.Worksheets.Add();
{{endregion}}



## Remove Worksheets

The __Worksheets__ collection of the workbook offers two methods for removing worksheets: __Remove()__ and __RemoveAt()__. The former method requires the worksheet name or the worksheet instance to be passed as an argument. The latter allows you specify the index of the worksheet you would like to remove.
        

__Example 2__ creates a workbook and adds four worksheets. All worksheets are with their default names: Sheet1, Sheet2, Sheet3 and Sheet4. The code further demonstrates how to remove three worksheets using all of the aforementioned remove methods.
        

#### __[C#] Example 2: Add and remove worksheets__

{{region cs-radspreadprocessing-working-with-worksheets-add-remove-worksheets_1}}
	Workbook workbook = new Workbook();
	workbook.Worksheets.Add(); // Sheet1
	Worksheet secondWorksheet = workbook.Worksheets.Add(); // Sheet2
	workbook.Worksheets.Add(); // Sheet3
	workbook.Worksheets.Add(); // Sheet4
	
	workbook.Worksheets.RemoveAt(3); // Removed Sheet4
	workbook.Worksheets.Remove("Sheet1"); // Removed Sheet1
	workbook.Worksheets.Remove(secondWorksheet); // Removed Sheet2
	// the only worksheet left is Sheet3
{{endregion}}


## Reorder Worksheets

If you would like to change the order the worksheets appear inside the workbook, you can use the **Move()** method of the **Sheets** collection. The method allows you to move one or more consecutive sheets to a specified position. In **Example 3**, you can see how you can insert 4 sheets and move the last one to the first position in the collection. When the workbook is visualized, the fourth sheet will be the first one visible in the sheet tabs.

#### __[C#] Example 3: Add and reorder worksheets__

{{region cs-radspreadprocessing-working-with-worksheets-add-remove-worksheets_2}}
	Workbook workbook = new Workbook();
	workbook.Worksheets.Add(); // Sheet1
	workbook.Worksheets.Add(); // Sheet2
	workbook.Worksheets.Add(); // Sheet3
	workbook.Worksheets.Add(); // Sheet4
	
	workbook.Sheets.Move(3, 1, 0); // Move the fourth sheet to the first place

{{endregion}}