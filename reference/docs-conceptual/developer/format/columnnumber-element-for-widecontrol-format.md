---
description: ColumnNumber Element for WideControl
ms.date: 08/20/2021
title: ColumnNumber Element for WideControl
---
# ColumnNumber Element for WideControl

Specifies the number of columns displayed in the wide view.

## Schema

- Configuration Element
- ViewDefinitions Element
- View Element
- WideControl Element
- ColumnNumber Element

## Syntax

```xml
<ColumnNumber>PositiveInteger</ColumnNumber>
```

## Attributes and Elements

The following sections describe attributes, child elements, and the parent element of the
`ColumnNumber` element.

### Attributes

None.

### Child Elements

None.

### Parent Elements

|Element|Description|
|-------------|-----------------|
|[WideControl Element](./widecontrol-element-format.md)|Defines a wide (single value) list format for the view.|

## Text Value

Specify a positive integer value.

## Remarks

When defining a wide view, you can add the `AutoSize` element or the `ColumnNumber` element, but you
cannot add both.

For more information about the components of a wide view, see [Creating a Wide View](./creating-a-wide-view.md).

For an example of a wide view, see [Wide View (Basic)](./wide-view-basic.md).

## See Also

[Autosize Element for WideControl](./autosize-element-for-widecontrol-format.md)

[Creating a Wide View](./creating-a-wide-view.md)

[Wide View (Basic)](./wide-view-basic.md)

[Writing a PowerShell Formatting File](./writing-a-powershell-formatting-file.md)
