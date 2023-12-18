# Home

This site contains documentation for a fictitious company.

## Page Contents

??? Collapsible include
    {%
    include-markdown 'includes/included-file.md'
    heading-offset=1
    %}

This is a normal include with a larger heading offset:
{%
include-markdown 'includes/included-file.md'
heading-offset=2
%}

## Code Highlighting

```powershell
Get-CimInstance -Class Win32_LogicalDisk |
    Select-Object -Property Name, @{
        label='FreeSpace'
        expression={($_.FreeSpace/1GB).ToString('F2')}
    }
```