---
title: Using Different Elements on a RadRibbonBar
page_title: Using Different Elements on a RadRibbonBar | UI for WinForms Documentation
description: Using Different Elements on a RadRibbonBar
slug: winforms/ribbonbar/getting-started/using-different-elements-on-a-radribbonbar
tags: using,different,elements,on,a,radribbonbar
published: True
position: 6
---

# Using Different Elements on a RadRibbonBar



You can build the user interface of a Telerik RadRibbonBar using a variety of different elements. In this tutorial, you will see how some of these elements can be placed and customized.

## Prepare an ImageList to be Used in the Telerik RadRibbonBar

1. Create a __RadRibbonForm__control by adding it by clicking on the 'Add New Item...'
            option in the context menu of the project or by changing the base class of a standard Windows Form to __RadRibbonForm.__

1. Open the designer of the __RadRibbonForm__

1. Drag a WinForms __ImageList__ component from the Toolbox to the form.
            In the area below the design surface, you will see __imageList1__. 

1. Using the Images Collection Editor, add the desired images to the ImageList. For more help with this task, see 
            [How to: Add or Remove ImageList Images with the Designer in the Visual Studio 2005](http://msdn2.microsoft.com/en-us/library/ms233674.aspx) documentation. 

>note A predefined list of images has been prepared for the purpose of this demonstration.
>


## Adding a Tab and a Group

1. Click __Add New Tab...__ to create a new tab. 

1. Type the word __Write__and press __Enter__. 

1. Click off the __Write__tab to deselect it. 

1. Select the __Write__tab again. 

1. Click __Add New Group...__ to create a new group.

1. Set the __Text__ property of the new group to __Clipboard__. ![ribbonbar-using-different-elements-on-a-radribbonbar 001](images/ribbonbar-using-different-elements-on-a-radribbonbar001.png)

## Add Elements

1. Right-click the __Clipboard__group and select __Add an item__, and then __RadButtonElement__.

1. Select the__Clipboard__group again and by right-clicking on it add a __Vertical Button Group__. 

1. Select the group and open the __Properties__window. Find the __ShowBorder__
            property and set it to __true__.

1. Select the __Vertical Button Group__and from its __Smart____Tag__execute the __Edit Items__action. 

1. Add three __RadButtonElement__instances in the button group:![ribbonbar-using-different-elements-on-a-radribbonbar 002](images/ribbonbar-using-different-elements-on-a-radribbonbar002.png)

## Customize the RadButtonElement

1. Select the __RadButtonElement__which is outside the __Button Group__.

1. Set the __TextImageRelation__ property to __ImageAboveText__.

1. Set an appropriate image by modifying the __Image__property. 

1. Set the __ImageAlignment__property to __MiddleCenter__. 

1. Set the __Text__ property to __Paste__and the __TextAlignment__
            property to __MiddleCenter__.

With an appropriate __Image__the __RadRibbonBar__should look similarly:![ribbonbar-using-different-elements-on-a-radribbonbar 003](images/ribbonbar-using-different-elements-on-a-radribbonbar003.png)

## Customize the RadButtonElements in the RadRibbonBarButtonGroup

1. Select the first __RadButtonElement__in the __RadRibbonBarButtonGroup.__

1. Set the __DisplayStyle__property to __Image__

1. Set the __ImageAlignment__property to __MiddleCenter__

1. Set the __Image__property with an appropriate image

1. Do the same for the rest elements in the __RadRibbonBarButtonGroup__so that the result looks similar to this:![ribbonbar-using-different-elements-on-a-radribbonbar 004](images/ribbonbar-using-different-elements-on-a-radribbonbar004.png)

## Adding a RadGalleryElement

1. Select the __RadRibbonBar__control and add another __RadRibbonBarGroup__
            called __Styles__in the 'Write'____tab. 

1. Select the __Styles__group, right-click on it and add a __RadGalleryElement__. 

1. Select the __RadGalleryElement__and open the __Properties__window of Visual Studio.
              Find the __Items__collection and add 6 __RadGalleryItem__instances.
            

1. Set appropriate images to all of the __RadGalleryItem__ instances.

1. For each __RadGalleryItem__set the __DisplayStyle__property to 
            __Image__so that no text appears.

1. Find the __MaxColumns__and __MaxRows__ properties of the
              __RadGalleryElement__and set their values to 2 and 5 respectively. The result should be similar to this:
            

>note For the purpose of this demonstration Office 2007 like images for the gallery have been used.
>
![ribbonbar-using-different-elements-on-a-radribbonbar 005](images/ribbonbar-using-different-elements-on-a-radribbonbar005.png)