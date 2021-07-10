# Statements

## Module

Top-level `Module` statements, without `=`, define root namespaces.

It's possible to alias a root `Module` as an item of another module by using the following syntax:

```
Module A = Qux.PersonalModule
```

## Namespace

Use `Namespace` keyword to declare root namespaces.

```
Namespace Qux.Foo
    ' declarations
End Namespace
```

## Import

Use either `Import` or `Imports` keyword at the header of a program to import modules.

```
Imports Qux.Foo

' aliasing (following lines are equivalent)
Imports N = Qux.Foo
Imports Qux.Foo As N
```

## Loop

Infinite loop statement.

```
Loop
    ' code
End Loop
```

## Operator

`Me` literal is available for `Get`/`Set`/`Iterator`. Syntax:

```
Operator +(a, b)

' i can be any numeric type
Operator Get(i As Long) As V
Operator Set(i As Long, value As V)

Operator Iterator
    ' use Yield operator
End Operator
```

## Property

Can be used in types as well as modules. `Let` is equivalent and can be also be used in modules.

```
Public _X As Double
Property Get X As Double
    _X = 10
End Property
Property Let X (value As Double)
    ' code
End Property
```

## Select type

```
Select Type o
    Case o As RegExp
        Print(o.Flags)
    Case d As Double
        Print("some double: " & d)
    Case Else
        Print("none")
End Select
```

## TypeAlias

Declare a type alias.

```
TypeAlias A = SomeType
```

## Return statement

Assignment-like syntax can be used as well as `Return` keyword to return value. Empty return can also be written as `Exit` keyword followed by context keyword (either `Exit Function`, `Exit Sub` or `Exit Property`).

## Call statement

Call statement, unlike with call operator, can omit parentheses.

```
A arguments
Call A arguments
```

## Let statement

```
A = 0
' redeclare A
Let A As New Dictionary
```

## Method

### Overriding

It is not a verify error if a method is overrided with extra optional parameters and/or contravariant return type.