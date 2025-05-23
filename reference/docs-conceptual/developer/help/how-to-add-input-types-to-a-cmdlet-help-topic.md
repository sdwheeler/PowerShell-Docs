---
description: How to add input types to a cmdlet help topic
ms.date: 07/10/2023
title: How to add input types to a cmdlet help topic
---
# How to add input types to a cmdlet help topic

[!INCLUDE [use-platyps](../../../includes/use-platyps.md)]

This section describes how to add an **INPUTS** section to a PowerShell cmdlet Help topic. The
**INPUTS** section lists the .NET classes of objects that the cmdlet accepts as input from the
pipeline, either by value or by property name.

There is no limit to the number of classes that you can add to an **INPUTS** section. The input
types are enclosed in a `<command:inputTypes>` node, with each class enclosed in a
`<command:inputType>` element.

The schema includes two `<maml:description>` elements in each `<command:inputType>` element.
However, the `Get-Help` cmdlet displays only the content of the
`<command:inputType>/<maml:description>` element.

Beginning in PowerShell 3.0, the `Get-Help` cmdlet displays the content of the `<maml:uri>` element.
This element lets you direct users to topics that describe the .NET class.

The following XML shows the `<maml:inputTypes>` node.

```xml
<command:inputTypes>
  <command:inputType>
    <dev:type>
      <maml:name> Class name </maml:name>
      <maml:uri>  URI of a topic that describes the class </maml:uri>
      <maml:description/>
    </dev:type>
    <maml:description>
      <maml:para> Brief description </maml:para>
    </maml:description>
  </command:inputType>
</command:inputTypes>
```

The following XML shows an example of using the `<maml:inputTypes>` node to document an input type.

```xml
<command:inputTypes>
  <command:inputType>
    <dev:type>
      <maml:name>System.DateTime</maml:name>
      <maml:uri>https://learn.microsoft.com/dotnet/api/system.datetime</maml:uri>
      <maml:description/>
    </dev:type>
    <maml:description>
      <maml:para> You can pipe a date to the Set-Date cmdlet. <maml:para>
    <maml:description>
  </command:inputType>
</command:inputTypes>
```
