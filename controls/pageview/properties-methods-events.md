---
title: Properties, Methods and Events
page_title: Properties, Methods and Events | RadPageView
description: RadPageView is yet another great addition to the Telerik UI for for WinForms suite. As the name implies, this control layouts pages of subcontrols in different views.
slug: winforms/pageview/properties-methods-events
tags: pageview
published: True
position: 10
---

# Properties

|Property|Description|
|----|----|
|**ViewMode**|Gets or sets the current mode of the view.|
|**SelectedPage**|Gets or sets the RadPageViewPage instance that is currently selected within the view.|
|**Pages**|Gets the collection of pages for this view.|
|**ViewElement**|Gets the current RadPageViewElement instance that represents the UI of the view.|
|**DefaultPage**|Gets or sets the default RadPageViewPage that will be loaded after EndInit of the control. If the DefaultPage is null the currently selected page will be loaded.|
|**ItemSizeMode**|Gets or sets the text orientation of the item within the owning RadPageViewElement instance.|
|**ItemSize**|Gets or sets the size of the items when ItemSizeMode of RadPageView is PageViewItemSizeMode.EqualSize.|
|**SelectionWrap**|Gets or sets whether the pages will be wrapped around when performing selection using the arrow keys. If the property is set to true, pressing the right arrow key when the last page is selected will result in selecting the first page.|
|**AllowShowFocusCues**|Indicates the focus cues visibility when available, based on the corresponding control type and the current UI state.|
|**ViewElement.UseMnemonic**|Determines whether ampersand character will be treated as mnemonic or not.|


# Methods

|Method|Description|
|----|----|
|**EnsurePageVisible**|Ensures that the passed page as an argument will be visible.|


# Events

|Event|Description|
|----|----|
|**ItemDropping**|Occurs when an item is about to be dropped over another item.|
|**ItemDropped**|Occurs when an item was dropped over another item.|
|**ItemCreating**|Raised when page item is about to be created.|
|**NewPageRequested**|Raised when the current mode of the view is about to change. Cancelable.|
|**ViewModeChanging**|Raised when the current mode of the view is about to change. Cancelable.|
|**ViewModeChanged**|Raised when the current mode of the view has changed.|
|**ItemListMenuDisplaying**|Raised when the built-in ItemsList menu is about to be displayed. Cancelable.|
|**ItemListMenuDisplayed**|Raised when the built-in ItemsList menu is displayed.|
|**PageAdding**|Raised when a new page is about to be added to the view. Cancelable.|
|**PageAdded**|Raised when a new page has been successfully added to the view.|
|**PageRemoving**|Raised when a page is about to be removed from the view. Cancelable.|
|**PageRemoved**|Raised when a page has been successfully removed from the view.|
|**PageIndexChanging**|Raised when a page is about to change its index. Cancelable.|
|**PageIndexChanged**|Raised when a page's index has been successfully changed.|
|**PagesClearing**|Raised when all pages are about to be removed from the view. Cancelable.|
|**PagesCleared**|Raised when all pages have been successfully removed from the view.|
|**PageExpanding**|Raised when the content of a RadPageViewPage is expanding. This event is only raised when the view mode of the control is set to ExplorerBar.|
|**PageExpanded**|Raised when the content of a RadPageViewPage is expanded. This event is only raised when the view mode of the control is set to ExplorerBar.|
|**PageCollapsing**|Raised when the content of a RadPageViewPage is collapsing. This event is only raised when the view mode of the control is set to ExplorerBar.|
|**PageCollapsed**|Raised when the content of a RadPageViewPage is collapsed. This event is only raised when the view mode of the control is set to ExplorerBar.|
|**SelectedPageChanging**|Raised when currently selected page has changed.|
|**SelectedPageChanged**|Raised when currently selected page has changed.|
|**SuspendEvents**|Temporary suspends event raising.|
|**ResumeEvents**|Resumes event raising, previously suspended by a SuspendEvents call.|

# See Also

* [Properties](http://docs.telerik.com/devtools/winforms/api/html/properties_t_telerik_wincontrols_ui_radpageview.htm)
* [Methods](http://docs.telerik.com/devtools/winforms/api/html/methods_t_telerik_wincontrols_ui_radpageview.htm)
* [Events](http://docs.telerik.com/devtools/winforms/api/html/events_t_telerik_wincontrols_ui_radpageview.htm)

