# Expressions

## Lambda

Either `Function` or `Sub` keyword can be used for lambdas, followed by explicit parentheses and body.

```
Let GreetFn = Sub(s) Print("Greetings, " & s & "!")
GreetFn "world"
```

## Operators

- `Or`: if operands are neither numeric or Boolean, then it selects a reference (e.g. `List?.Map(...) Or {}`).
- `If`: `If(condition, arg1, arg2)`
- `ClosureOf m` results in method reference.
- Comparison `x <> y` is the reverse of `x = y`. `IsNot` and `Is` are equivalent operators.

## Structure initializer

If a structure (not a class) has no constructor and all members are public, object initializer may be used as an initializer.

```
Let o As New C {
    SomeField = 10,
    AnotherField = 10,
}
```

Inferred syntax can be used:

```
Let o As C?
o = {
    SomeField = 10,
    AnotherField = 10,
}
```

## Collection initializer

Use the `#` character followed by curly braces (`{}`) to initialize a Collection:

```
L = { E1, ...S, }
```