---
description: SelectionCondition Element for EntrySelectedBy for TableControl
ms.date: 08/25/2021
title: SelectionCondition Element for EntrySelectedBy for TableControl
---
# SelectionCondition Element for EntrySelectedBy for TableControl

Defines the condition that must exist to use for this definition of the table view. There is no
limit to the number of selection conditions that can be specified for a table definition.

## Schema

- Configuration Element
- ViewDefinitions Element
- View Element
- TableControl Element
- TableRowEntries Element
- TableRowEntry Element
- EntrySelectedBy Element
- SelectionCondition Element

## Syntax

```xml
<SelectionCondition>
  <TypeName>Nameof.NetType</TypeName>
  <SelectionSetName>NameofSelectionSet</SelectionSetName>
  <PropertyName>.NetTypeProperty</PropertyName>
  <ScriptBlock>ScriptToEvaluate</ScriptBlock>
</SelectionCondition>
```

## Attributes and Elements

The following sections describe attributes, child elements, and the parent element of the
SelectionCondition element.

### Attributes

None.

### Child Elements

|Element|Description|
|-------------|-----------------|
|[PropertyName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./propertyname-element-for-selectioncondition-for-entryselectedby-for-tablerowentry-format.md)|Optional element.<br /><br /> Specifies the .NET property that triggers the condition.|
|[ScriptBlock Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./scriptblock-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)|Optional element.<br /><br /> Specifies the script that triggers the condition.|
|[SelectionSetName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./selectionsetname-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)|Optional element.<br /><br /> Specifies the set of .NET types that trigger the condition.|
|[TypeName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./typename-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)|Optional element.<br /><br /> Specifies a .NET type that triggers the condition.|

### Parent Elements

|Element|Description|
|-------------|-----------------|
|[EntrySelectedBy Element for TableRowEntry](./entryselectedby-element-for-tablerowentry-for-tablecontrol-format.md)|Defines the .NET types that use this table entry or the condition that must exist for this entry to be used.|

## Remarks

Each list entry must have at least one type name, selection set, or selection condition defined.

When you are defining a selection condition, the following requirements apply:

- The selection condition must specify a least one property name or a script block, but cannot
  specify both.
- The selection condition can specify any number of .NET types or selection sets, but cannot specify
  both.

For more information about how to use selection conditions, see [Defining Conditions for when a View Entry or Item is Used](./defining-conditions-for-displaying-data.md).

For more information about the components of a table view, see [Creating a Table View](./creating-a-table-view.md).

## See Also

[Creating a Table View](./creating-a-table-view.md)

[Defining Conditions for When Data Is Displayed](./defining-conditions-for-displaying-data.md)

[EntrySelectedBy Element](./entryselectedby-element-for-tablerowentry-for-tablecontrol-format.md)

[PropertyName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./propertyname-element-for-selectioncondition-for-entryselectedby-for-tablerowentry-format.md)

[ScriptBlock Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./scriptblock-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)

[SelectionSetName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./selectionsetname-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)

[TypeName Element for SelectionCondition for EntrySelectedBy for TableRowEntry](./typename-element-for-selectioncondition-for-entryselectedby-for-tablecontrol-format.md)

[Writing a Windows PowerShell Formatting and Types File](./writing-a-powershell-formatting-file.md)
