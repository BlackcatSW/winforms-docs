---
title: Resizing columns programmatically
page_title: Resizing columns programmatically | RadGridView
description: Set the columns size either manually or use the API to size the columns according to their content.
slug: winforms/gridview/columns/resizing-columns-programatically
tags: resizing,columns,programmatically
published: True
position: 6
previous_url: gridview-columns-resizing-columns-programatically
---

# Resizing columns programmatically

## Resizing columns

By default, the columns inside **RadGridView** are resizable. The user is able to easily change the column's width by positioning the mouse over the column's vertical grid line and dragging it until the desired size is achieved. 

![gridview-columns-rezise-columns001](images/gridview-columns-rezise-columns001.gif)

## Disabling resizing

There are two ways to disable resizing of columns in the user interface:

* To restrict resizing of all columns by the user set the __AllowColumnResize__ property of **RadGridView** to *false*

#### Disable resizing

{{source=..\SamplesCS\GridView\Columns\ResizingColumns.cs region=AllowColumnResize}} 
{{source=..\SamplesVB\GridView\Columns\ResizingColumns.vb region=AllowColumnResize}} 

````C#
this.radGridView1.AllowColumnResize = false;

````
````VB.NET
Me.RadGridView1.AllowColumnResize = False

````

{{endregion}}

* To restrict resizing of a particular column set the __AllowResize__ property of the column to *false*.

#### Disable resizing for a specified column

{{source=..\SamplesCS\GridView\Columns\ResizingColumns.cs region=AllowResize}} 
{{source=..\SamplesVB\GridView\Columns\ResizingColumns.vb region=AllowResize}} 

````C#
this.radGridView1.Columns["Photo"].AllowResize = false;

````
````VB.NET
Me.RadGridView1.Columns("Photo").AllowResize = False

````

{{endregion}}

## Programmatically resizing columns

The width of columns can be set individually, per column. Note that the visible width will always include some amount of data even when set to very small amounts. To resize the columns programmatically you can use the __Width__ property. For example: 

#### Resize a column programmatically

{{source=..\SamplesCS\GridView\Columns\ResizingColumns.cs region=resizingColumn}} 
{{source=..\SamplesVB\GridView\Columns\ResizingColumns.vb region=resizingColumn}} 

````C#
this.radGridView1.Columns["Photo"].Width = 100;

````
````VB.NET
Me.RadGridView1.Columns("Photo").Width = 100

````

{{endregion}}

You can restrict the possible values of the __Width__ property by setting the __MinWidth__ and __MaxWidth__ properties. The __MinWidth__ property sets a limit on how narrow the column can be resized. The __MaxWidth__ property determines the limit on how the column width can grow.

>note The **DpiScale** property gives the effective Dpi scaling of the control. The **Width** property of the columns returns a value considering the **DpiScale**.

## Column Auto-Sizing

There are two ways to auto size the columns:

### AutoSizeColumnsMode

Columns can automatically fill the entire width of the grid. Just set the __AutoSizeColumnsMode__ property of the desired template to GridViewAutoSizeColumnsMode.*Fill*.

### Best fit

The column widths can be set to fit its content by using the GridViewTemplate.__BestFitColumns__ or GridViewDataColumn.__BestFit__ methods. This mode distributes algorithm that attempts to fit in the header text and column data for all visible rows.

>note Before using one of the best-fit methods, make sure that the grid is populated with data. Considering the content in the data rows, the columns' width will be calculated.

The user can perform the best fit operation:

* By using the context menu of the header cell

* By double clicking of the left or right header edge 

![](images/gridview-columns-rezise-columns003.png)

You can customize the execution of the algorithm of a concrete column by setting the __AutoSizeMode__ property on the desired column. Here are the available options:

* BestFitColumnMode.__None__ - The column's width does not automatically adjust.

* BestFitColumnMode.__AllCells__ - The column's width adjusts to fit the contents of all cells in the control.

* BestFitColumnMode.__DisplayedDataCells__ - The column's width adjusts to fit the contents of the displayed data cells.

* BestFitColumnMode.__HeaderCells__ - The column's width adjusts to fit the contents of the header cell.

* BestFitColumnMode.__FilterCells__ - The column's width adjusts to fit the contents of the filter cell.

* BestFitColumnMode.__SummaryRowCells__ - The column's width adjusts to fit the contents of the summary row cell.

* BestFitColumnMode.__SystemCells__ - The column's width adjusts to fit the contents of the system cells.

* BestFitColumnMode.__DisplayedCells__ - The column's width adjusts to fit the contents of the displayed cells.

## Resizing events

When the user resizes the column, the __ColumnWidthChanging__ event is fired and if it is not canceled, the __ColumnWidthChanged__ event fires after the resize operation is completed.

# See Also
* [Accessing and Iterating through Columns]({%slug winforms/gridview/columns/accessing-and-iterating-through-columns%})

* [Calculated Columns (Column Expressions)]({%slug winforms/gridview/columns/calculated-columns-(column-expressions)%})

* [Overview]({%slug winforms/gridview/columns%})

* [Converting Data Types]({%slug winforms/gridview/columns/converting-data-types%})

* [Data Formatting]({%slug winforms/gridview/columns/data-formatting%})

* [Generating Columns]({%slug winforms/gridview/columns/generating-columns%})

* [GridViewColumn]({%slug winforms/gridview/columns/column-types/gridviewcolumn%})

* [GridViewDataColumn]({%slug winforms/gridview/columns/column-types/gridviewdatacolumn%})

