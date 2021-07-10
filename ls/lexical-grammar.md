# Lexical grammar

## Comments

```
' some comment
```

## Identifiers

- RegExp:`(?i)[a-z][a-z0-9_]*`
- RegExp: `(?i)_[a-z0-9_]*`
- RegExp: `\[[a-z0-9_]+\]` (escaped identifier)

## Keywords

```
And
As
Async
Await
Call
Case
Catch
Class
ClosureOf
Continue
CType
Do
Else
ElseIf
Empty
End
Enum
Eqv
Exit
False
Finally
For
Function
Get
GetType
Global
If
Imp
Implements
Import
Imports
In
Inherits
Interface
Internal
Is
IsNot
Let
Loop
Me
Mod
Module
Namespace
Native
New
Next
Not
Nothing
NotInheritable
NotOverridable
Null
Of
Operator
Or
Overrides
Private
Property
Protected
Public
ReadOnly
Return
Select
Set
Shared
Step
Structure
Sub
Super
Then
Throw
To
True
Try
TryCast
TypeAlias
TypeOf
Until
Wend
When
Where
While
With
Xor
Yield
```

## Context keywords

- `Any`
  - Used as a type expression.
- `Each`
  - Used by `For Each`
- `Embed`
  - Used by `Embed "src"`
- `Include`
  - Used by `Include "src"`
- `IteratorHasNext`
  - Used by `Operator IteratorHasNext`
- `IteratorNext`
  - Used by `Operator IteratorNext`
- `Type`
  - Used by `Select Type`

## Punctuators

- `=`
- `<>`
- `(` `)`
- `{` `}`
- `#`:
  - Used for Collection initializer: `#{}`.
- `:`
  - Statement separator
- `.`
- `,`
- `?`
  - Nullable type expression.
  - Optional property/element chain (`?.x` and `?(index)`).
- `...`
  - Rest parameter
  - Spread collection in collection literal
- `&`
  - String concatenation
- `_`
  - Line continuation
  - Ignore destructuring element
- `<` `>` `<=` `>=`
- `+` `-` `*` `/` `^`
- `<<` `>>` `>>>`
- Compound assignment operator
  - `+=` `-=` `*=` `/=` `^=` `&=`
  - `<<=` `>>=` `>>>=`