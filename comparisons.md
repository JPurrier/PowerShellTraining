# Comparison Operators

Comparison operators let you specify conditions for comparing values and finding values that match specified patterns.

Lets look at and example:
```
$one = 1
$two = 2

# Lets do some comparrisons
$two -gt $one
$one -lt $two
$one -ne $two
$two -eq $two
```

| Type	| Operators | Description |
| ------|:---------:|-------------|
|Equality |	-eq |	equals|
||-ne |	not | equals |
||-gt|	greater than|
||-ge|	greater than or equal|
||-lt |	less than|
||-le	|less than or equal||
|Matching	|-like|	Returns true when string matches wildcard|
|||pattern|
||-notlike|	Returns true when string does not match|

REF: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_comparison_operators?view=powershell-7

End of unit demo:
![comparison_e2e.gif](images/comparison_e2e.gif)


7. [Indexing](indexing.md)