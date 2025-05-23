---
description: TypeName Element for SelectionCondition for EntrySelectedBy for WideControl
ms.date: 08/25/2021
title: TypeName Element for SelectionCondition for EntrySelectedBy for WideControl
---
# TypeName Element for SelectionCondition for EntrySelectedBy for WideControl

Specifies a .NET type that triggers the condition. When this type is present, the definition is
used.

## Schema

- Configuration Element
- ViewDefinitions Element
- View Element
- WideControl Element
- WideEntries Element
- WideEntry Element
- EntrySelectedBy Element
- SelectionCondition Element
- TypeName Element

## Syntax

```xml
<TypeName>Nameof.NetType</TypeName>
```

## Attributes and Elements

The following sections describe attributes, child elements, and the parent element of the `TypeName`
element.

### Attributes

None.

### Child Elements

None.

### Parent Elements

|Element|Description|
|-------------|-----------------|
|[SelectionCondition Element for EntrySelectedBy for WideEntry](./selectioncondition-element-for-entryselectedby-for-widecontrol-format.md)|Defines the condition that must exist for this wide entry to be used.|

## Text Value

Specify the fully qualified name of the .NET type, such as `System.IO.DirectoryInfo`.

## Remarks

The selection condition can specify a .NET type or a selection set, but cannot specify both. For
more information about how to use selection conditions, see [Defining Conditions for when Data is Displayed](./defining-conditions-for-displaying-data.md).

For more information about other components of a wide view, see [Creating a Wide View](./creating-a-wide-view.md).

## See Also

[Creating a Wide View](./creating-a-wide-view.md)

[Defining Conditions for When Data Is Displayed](./defining-conditions-for-displaying-data.md)

[SelectionCondition Element for EntrySelectedBy for WideEntry](./selectioncondition-element-for-entryselectedby-for-widecontrol-format.md)

[SelectionSetName Element for SelectionCondition for EntrySelectedBy for WideEntry](./selectionsetname-element-for-selectioncondition-for-entryselectedby-for-wideentry-format.md)

[Writing a PowerShell Formatting File](./writing-a-powershell-formatting-file.md)
