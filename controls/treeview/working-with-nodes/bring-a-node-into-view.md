---
title: Bring a Node into View
page_title: Bring a Node into View | RadTreeView
description: This article shows how one can use the BringIntoView method in order to navigate to a particular node.
slug: winforms/treeview/working-with-nodes/bring-a-node-into-view
tags: bring,a,node,into,view
published: True
position: 3
previous_url: treeview-working-with-nodes-bring-a-node-into-view
---

# Bring a Node into View


In cases where you have a tree view with many nodes and limited space on the form, you need to scroll the control in order to find a specific node. __RadTreeView__ control handles this automatically for you. To scroll the control to a node use the __BringIntoView__ method.

{{source=..\SamplesCS\TreeView\WorkingWithNodes\WorkingWithNodes1.cs region=bringIntoView}} 
{{source=..\SamplesVB\TreeView\WorkingWithNodes\WorkingWithNodes1.vb region=bringIntoView}} 

````C#
RadTreeNode lastRootNode = radTreeView1.Nodes[radTreeView1.Nodes.Count - 1];
radTreeView1.BringIntoView(lastRootNode.Nodes[lastRootNode.Nodes.Count - 1]);

````
````VB.NET
Dim lastRootNode As RadTreeNode = RadTreeView1.Nodes(RadTreeView1.Nodes.Count - 1)
RadTreeView1.BringIntoView(lastRootNode.Nodes(lastRootNode.Nodes.Count - 1))

````

{{endregion}}

>important The **BringIntoView** method does not select the node!
>

>note The **RadTreeViewElement** class defines an **AutoScrollOnClick** property which is by default set to *true*. This property determines whether to scroll horizontally the control ensuring that the clicked node is visible.
> 

# See Also
* [Adding and Removing Nodes]({%slug winforms/treeview/working-with-nodes/adding-and-removing-nodes%})

* [Custom Filtering]({%slug winforms/treeview/working-with-nodes/custom-filtering%})

* [Custom Nodes]({%slug winforms/treeview/working-with-nodes/custom-nodes%})

* [Custom Sorting]({%slug winforms/treeview/working-with-nodes/custom-sorting%})

* [Events]({%slug winforms/treeview/working-with-nodes/events%})

* [Filtering Nodes]({%slug winforms/treeview/working-with-nodes/filtering-nodes%})

 