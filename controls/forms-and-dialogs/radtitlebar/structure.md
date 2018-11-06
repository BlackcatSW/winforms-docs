---
title: Structure
page_title: Structure | RadTitleBar
description: RadTitleBar control is used in forms and provides functionality for dragging, minimizing, maximizing and closing the form. This control is internally used by RadForm.
slug: winforms/forms-and-dialogs/radtitlebar/structure
tags: radtitlebar
published: True
position: 1 
---

# Structure

This article describes the inner structure and organization of the elements which build the __RadTitleBar__ control.
        
>caption Figure 1: RadTitleBar's elements hierarchy

![forms-and-dialogs-titlebar-structure 001](images/forms-and-dialogs-titlebar-structure001.png)

>caption Figure 2: RadTitleBar's structure

![forms-and-dialogs-titlebar-structure 002](images/forms-and-dialogs-titlebar-structure002.png)

1. __RadTitleBarElement__  
	1.1 __FillPrimitive__: Represents the fill of __RadTitleBar__    
	1.2 __DockLayoutPanel__: Holds the system buttons and text element   
&nbsp;&nbsp;&nbsp;&nbsp; 1.2.1 __TextPrimitive__: Represents the text of __RadTitleBar__  
&nbsp;&nbsp;&nbsp;&nbsp; 1.2.2 __StackLayoutElement__: Holds the system buttons   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1.2.2.1 __RadImageButtonElement__: Represents each of the system buttons.

# See Also

* [Help Button]({%slug winforms/forms-and-dialogs/radtitlebar/help-button%})	