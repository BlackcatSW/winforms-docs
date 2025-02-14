---
title: Grouping
page_title: Grouping - WinForms TreeMap Control
description: Get familiar with the grouping functionality in the WinForms TreeMap's control.  
slug: winforms-treemap-grouping
tags: treemap, grouping
published: True
position: 1
---

# Grouping

**RadTreeMap** supports grouping for its data items combining the pieces belonging to the same group with a similar color/palette. 

When using [unbound mode]({%slug treemap-unbound-mode%}), it is necessary to add a **TreeMapDataItemGroup** specifying the group **Text** and **LegendTitle**. Then, specify the **Group** property for each **TreeMapDataItem**. The group items can be added either at design time via the *TreeMapDataItemGroup Collection Editor* or at run time. Read more in the following help article: [Unbound Mode]({%slug treemap-unbound-mode%}). 

>caption Adding Groups at Design Time

![winforms-treemap-grouping 001](images/winforms-treemap-grouping001.png)

When using [bound mode]({%slug treemap-data-binding%}), once the **RadTreeMap** is populated with data, it is possible to add a new **GroupDescriptor** to the **GroupDescriptors** collection:

>caption RadTreeMap with no grouping

![winforms-treemap-grouping 002](images/winforms-treemap-grouping002.png)

>caption RadTreeMap grouped by CategoryID 

![winforms-treemap-grouping 003](images/winforms-treemap-grouping003.png)

{{source=..\SamplesCS\TreeMap\TreeMapGettingStarted.cs region=Grouping}} 
{{source=..\SamplesVB\TreeMap\TreeMapGettingStarted.vb region=Grouping}} 

````C#

this.radTreeMap1.DisplayMember = "ProductName";
this.radTreeMap1.ValueMember = "ProductID";
this.radTreeMap1.DataSource = this.productsBindingSource;
this.radTreeMap1.GroupDescriptors.Add("CategoryID", ListSortDirection.Descending);          

````
````VB.NET

Me.radTreeMap1.DisplayMember = "ProductName"
Me.radTreeMap1.ValueMember = "ProductID"
Me.radTreeMap1.DataSource = Me.productsBindingSource
Me.radTreeMap1.GroupDescriptors.Add("CategoryID", ListSortDirection.Ascending)

````

{{endregion}} 

 
# See Also

* [Structure]({%slug winforms-treemap-structure%}) 

* [Layout Strategies]({%slug treemap-layout-strategies%})

* [Colorizers]({%slug treemap-colorizers%})

