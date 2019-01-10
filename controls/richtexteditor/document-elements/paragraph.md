---
title: Paragraph
page_title: Paragraph | RadRichTextEditor
description: RadRichTextEditor is a control that allows you to display and edit rich text content including sections, paragraphs, spans, italic text, bold text, inline images, tables etc.
slug: winforms/richtexteditor-/document-elements/paragraph
tags: paragraph
published: True
position: 2
previous_url: richtexteditor-document-elements-paragraph
---

# Paragraph 

The paragraph class allows you to separate the content into paragraphs. It is responsible for displaying inline elements such as __Span__, __HyperlinkRangeStart__ and __End__, __InlineImage__ etc. You are also able to configure the appearance of the paragraph by modifying its parameters.
      
This topic will explain you how to:

* [Use Paragraphs](#use-paragraphs)

* [Add inline elements to a Paragraph](#add-inline-elements-to-a-paragraph)

* [Customize the Paragraph](#customize-the-paragraph)

## Use Paragraphs

The __Paragraph__ can be used only in the context of a [Section]({%slug winforms/richtexteditor-/document-elements/section%}) or a **TableCell** element. The section exposes a collection of **Blocks**, to which the paragraphs can be added.

{{source=..\SamplesCS\RichTextEditor\DocumentElements\ParagraphCode.cs region=section}} 
{{source=..\SamplesVB\RichTextEditor\DocumentElements\ParagraphCode.vb region=section}} 

````C#
            
Section section = new Section();
Paragraph paragraph = new Paragraph();          
section.Blocks.Add(paragraph);
RadDocument document = new RadDocument();
document.Sections.Add(section);
            
this.radRichTextEditor1.Document = document;

````
````VB.NET
Dim section As New Section()
Dim paragraph As New Paragraph()    
section.Blocks.Add(paragraph)
Dim document As New RadDocument()
document.Sections.Add(section)
Me.radRichTextEditor1.Document = document

````

{{endregion}} 

## Add inline elements to a Paragraph

To add inline elements such as **Span**, **HyperlinkRangeStart** and **End**, or **InlineImage** you have to use the **Inlines** collection of the **Paragraph**.

{{source=..\SamplesCS\RichTextEditor\DocumentElements\ParagraphCode.cs region=inline}} 
{{source=..\SamplesVB\RichTextEditor\DocumentElements\ParagraphCode.vb region=inline}} 

````C#
            
Section section = new Section();
Paragraph paragraph = new Paragraph();
Span span = new Span("Span declared in code-behind");
paragraph.Inlines.Add(span);
section.Blocks.Add(paragraph);
RadDocument document = new RadDocument();
document.Sections.Add(section);
    
this.radRichTextEditor1.Document = document;

````
````VB.NET
Dim section As New Section()
Dim paragraph As New Paragraph()
Dim span As New Span("Span declared in code-behind")
paragraph.Inlines.Add(span)
section.Blocks.Add(paragraph)
Dim document As New RadDocument()
document.Sections.Add(section)
Me.radRichTextEditor1.Document = document

````

{{endregion}} 

## Customize the Paragraph

The __Paragraph__ exposes several properties that allow you to customize the layout of the elements placed underneath it. Here is a list of them:
        
* __FontSize__ - represents the font size of the text inside the __Paragraph__. If not explicitly set to its child elements, they inherit its value.

*  __LineSpacing__ - specifies the value for the space between the lines.

* __LineSpacingType - specifies the type of spacing:__

	* __AtLeast -__ the space between the lines should be equal or greater than the value of the __LineSpacing__ property.
                
	* __Auto -__ the space between the lines is determined automatically.
                
	* __Exact -__ the space between the lines should be equal to the value of the __LineSpacing__ property.

* __LeftIndent -__ represents the size of the indent to the left size of the __Paragraph__. The indent gets applied together with the respective margins to the layout.            

* __RightIndent__ - represents the size of the indent to the right size of the __Paragraph__. The indent gets applied together with the respective margins to the layout.            

* __SpacingAfter__ - represents the size of the empty space after the __Paragraph__.            

* __SpacingBefore__ - represents the size of the empty space before the __Paragraph__.            

* __TextAlignment__ - represents the alignment of the text inside the __Paragraph__.
            

# See Also

 * [Document Elements]({%slug winforms/richtexteditor-/document-elements%})

 * [RadDocument]({%slug winforms/richtexteditor-/document-elements/raddocument%})

 * [Section]({%slug winforms/richtexteditor-/document-elements/section%})

 * [Span]({%slug winforms/richtexteditor-/document-elements/span%})

 * [Inline Image]({%slug winforms/richtexteditor-/document-elements/inline-image%})

 * [Hyperlink]({%slug winforms/richtexteditor-/features/hyperlink%})
