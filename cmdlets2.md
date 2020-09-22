# >_ CMDLETS Continued..

## Finding CMDLETS

Ok so we know cmdlets are powerfull and useful but how do we find them? Ok well first thing to know is that cmdlets use a structure of verb-noun and their are a set of approved verbs.

For example most commands that ```Get``` information in a read-only fashion will begin with ```Get```

Examples:
```
Get-Process
Get-ChildItem
Get-Date
```

Lets assume you have a rough idea of what your looking for such as you want information about a DNS but you dont now the command. Powershell can help with that.

```Get-Command "*DNS*"```

This will provide a long list of DNS commands. Helpful but we still need to narrow this list down. We know we just want to get information not change settings. Therefore its likely we need a ```Get``` command. So lets filter these results by piping the information to Where-Object (we will go into greater detail on this later in the courese).

```Get-Command "*DNS*" | Where-Object {$_.Name -like "*Get*"}```

This gives us a list of DNS commands that start with Get.

We could use the simpler option of ```Get-Command "Get-DNS*"``` though this might not return all DNS commands. 

Lets assume we have found a command that looks interesting to use ```Get-DNSClient``` but we want to find out more information about the command before we run it.

```Get-Help``` to the rescue:
```Get-Help Get-DNSClient``` 
Ok so now we know what it does and the syntax, but we want to get examples. We have two options local examples or online.
```
Get-Help Get-DNSClient -examples
Get-Help Get-DNSClient -online
``` 

4. [Applying Logic To commands](logic.md)