---
description: Describes the `parallel` keyword, which runs the activities in a workflow in parallel.
Locale: en-US
ms.date: 06/09/2017
online version: https://learn.microsoft.com/powershell/module/psworkflow/about/about_parallel?view=powershell-5.1&WT.mc_id=ps-gethelp
schema: 2.0.0
title: about_Parallel
---
# about_Parallel

## SHORT DESCRIPTION
Describes the `parallel` keyword, which runs the activities in a workflow in parallel.

## LONG DESCRIPTION

The `parallel` keyword runs workflow activities in parallel. This keyword is valid only in  Windows PowerShell  Workflow.

### SYNTAX

```
workflow <Verb-Noun> {
     parallel {
          [<Activity>]
          [<Activity>]
        ...
     }
 }
```

## DETAILED DESCRIPTION

The commands in a `parallel` script block can run concurrently. The order in which they run is not determined.

For example, the following workflow includes a `parallel` script block that runs activities that get processes and services on the computer. Because the Get-Process and Get-Service commands are independent of each other, they can run concurrently and in any order.

```powershell
workflow Test-Workflow {
    parallel {
         Get-Process
         Get-Service
    }
}
```

Running commands in parallel is very efficient and reduces the time it takes to complete a workflow significantly.

To run selected commands in a `parallel` script block in sequential order, use the `sequence` keyword. For more information, see [about_Sequence](about_Sequence.md).

To run a script block on items in a collection, use the `foreach` or
`foreach -Parallel` keywords.

## See Also

- [about_Foreach](../../Microsoft.PowerShell.Core/About/about_Foreach.md)
- [about_Foreach-Parallel](about_Foreach-Parallel.md)
- [about_Language_Keywords](../../Microsoft.PowerShell.Core/About/about_Language_Keywords.md)
- [about_Sequence](about_Sequence.md)
- [about_Workflows](about_workflows.md)
- ["Writing a Script Workflow"](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj574157(v=ws.11))
