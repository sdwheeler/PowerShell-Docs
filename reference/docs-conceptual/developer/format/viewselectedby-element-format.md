---
description: ViewSelectedBy Element
ms.date: 08/25/2021
title: ViewSelectedBy Element
---
# ViewSelectedBy Element

Defines the .NET objects that are displayed by the view. Each view must specify at least one .NET
object.

## Schema

- ViewDefinitions Element
- View Element
- ViewSelectedBy Element

## Syntax

```xml
<ViewSelectedBy>
  <TypeName>Nameof.NetType</TypeName>
  <SelectionSetName>SelectionSet</SelectionSetName>
</ViewSelectedBy>
```

## Attributes and Elements

The following sections describe the attributes, child elements, and parent element of the
`ViewSelectedBy` element. This element must contain at least one `TypeName` or `SelectionSetName`
child element. There is no limit to the number of child elements that can be specified nor is their
order significant.

### Attributes

None.

### Child Elements

|Element|Description|
|-------------|-----------------|
|[TypeName Element for ViewSelectedBy](./typename-element-for-viewselectedby-format.md)|Optional element.<br /><br /> Specifies a .NET object that is displayed by the view.|
|[SelectionSetName Element for ViewSelectedBy](./selectionsetname-element-for-viewselectedby-format.md)|Optional element.<br /><br /> Specifies a set of .NET objects that are displayed by the view.|

### Parent Elements

|Element|Description|
|-------------|-----------------|
|[View Element](./view-element-format.md)|Defines a view that displays one or more .NET objects.|

## Remarks

For more information about how this element is used in different views, see [Table View Components](./creating-a-table-view.md), [List View Components](./creating-a-list-view.md), [Wide View Components](./creating-a-wide-view.md), and [Custom Control Components](./creating-custom-controls.md).

The `SelectionSetName` element is used when the formatting file defines a set of objects that are
displayed by multiple views. For more information about how selection sets are defined and
referenced, see [Defining Sets of Objects](./defining-selection-sets.md).

## Example

The following example shows how to specify the [System.ServiceProcess.ServiceController](/dotnet/api/System.ServiceProcess.ServiceController)
object for a list view. The same schema is used for table, wide, and custom views.

```xml
<View>
  <Name>System.ServiceProcess.ServiceController</Name>
  <ViewSelectedBy>
    <TypeName>System.ServiceProcess.ServiceController</TypeName>
  </ViewSelectedBy>
  <ListControl>...</ListControl>
</View>
```

## See Also

[Creating a List View](./creating-a-list-view.md)

[Creating a Table View](./creating-a-table-view.md)

[Creating a Wide View](./creating-a-wide-view.md)

[Creating Custom Controls](./creating-custom-controls.md)

[Defining Selection Sets](./defining-selection-sets.md)

[SelectionSetName Element for ViewSelectedBy](./selectionsetname-element-for-viewselectedby-format.md)

[TypeName Element](./typename-element-for-viewselectedby-format.md)

[Writing a PowerShell Formatting File](./writing-a-powershell-formatting-file.md)
