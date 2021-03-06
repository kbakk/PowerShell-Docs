---
ms.date:  2017-06-09
schema:  2.0.0
locale:  en-us
keywords:  powershell,cmdlet
external help file:  Pester-help.xml
---

# Context

## SYNOPSIS
Provides logical grouping of It blocks within a single Describe block.
Any Mocks defined
inside a Context are removed at the end of the Context scope, as are any files or folders
added to the TestDrive during the Context block's execution.
Any BeforeEach or AfterEach
blocks defined inside a Context also only apply to tests within that Context .

## SYNTAX

```
Context [-Name] <String> [[-Fixture] <ScriptBlock>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
function Add-Numbers($a, $b) {
```

return $a + $b
}

Describe "Add-Numbers" {

    Context "when root does not exist" {
         It "..." { ...
}
    }

    Context "when root does exist" {
        It "..." { ...
}
        It "..." { ...
}
        It "..." { ...
}
    }
}

## PARAMETERS

### -Name
The name of the Context.
This is a phrase describing a set of tests within a describe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fixture
Script that is executed.
This may include setup specific to the context and one or more It
blocks that validate the expected outcomes.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: $(Throw "No test script block is provided. (Have you put the open curly brace on the next line?)")
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Describe](Describe.md)

[It](It.md)

[BeforeEach](BeforeEach.md)

[AfterEach](AfterEach.md)

[about_Should]()

[about_Mocking]()

[about_TestDrive]()