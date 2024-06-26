---
sidebar_position: 2
title: Spacer Form Field
---


The **spacer** form field type provides a dropdown list of h1 to h6 as options.

- **type** (mandatory) must be *spacer*.
- **name** (mandatory) is the unique name of the field.
- **label** (mandatory) is the text to use as a spacer.
- **description** (optional) (translatable) is text that will be shown as a tooltip when the user moves the mouse over the field.
- **hr** (optional) is whether to display a horizontal rule ('true' or 'false'). If this attribute is 'true', the label attribute will be ignored. 
- **class** (optional) is a CSS class name for the HTML form field.

Implemented by: libraries/src/Form/SpacerField.php

## Example XML parameter definition

```xml
<field
        type="spacer" 
        name="myspacer" 
        hr="true"
/>
```

You can replace the basic horizontal line with a title which can be used to group parameters. For example:

```xml
<field
        type="spacer" 
        name="myspacer" 
        label="Advanced parameters"
/>
```
You can also place translatable text into the label attribute: 
```xml
<field 
        type="spacer" 
        name="myspacer" 
        class="text"
        label="PLG_TINY_FIELD_NAME_EXTENDED_LABEL"
/>
```
Note that you can also include HTML markup but it must be encoded. For example, to put the text into bold you can use: 
```xml
<field 
        type="spacer" 
        name="myspacer" 
        label="&lt;b&gt;Advanced parameters&lt;/b&gt;" 
/>
```

**You cannot combine the hr and label attributes.** To define a spacer with both a horizontal rule and a label, use an encoded `<hr/>` in the label attribute: 

```xml
<field 
        type="spacer" 
        name="myspacer" 
        label="&lt;hr/&gt;More parameters" 
/>
```