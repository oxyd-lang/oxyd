# Syntax

### Structure

## Variables

The structure of a variable is as follows:

```go
(x := value)
```

- `x`: Name of the variable.
- `:=`: Operator to infer the type of the variable.
- `value`: Value of the variable.

```go
(y: type = value)
```

- `y`: Name of the variable.
- `type`: Type of the variable.
- `=`: Operator to define a variable.
- `value`: Value of the variable.

```go
(var {
    x := value,
    y := value,
    z := value,
})
```

- `var`: Keyword to define multiple variables.
- `{}`: Block of variables.
- `x`, `y`, `z`: Names of the variables.
- `:=`: Operator to infer the type of the variable.
- `value`: Value of the variable.

More examples:

```go
(x := 10) // infer type
```

```go
(var x: int = 10) // define type
```

```go
(var {
    x: float64 = 10.5,
    y: int = 5,
    z: string = "oxyd"
})
```


## Functions

The structure of a function is as follows:

```go
(fn x [y: type, z: type] { } -> type)
```

- `fn`: Keyword to define a function.
- `x`: Name of the function.
- `y`, `z`: Parameters of the function.
- First and second `type`: Type of the parameters.
- `{}`: Block of the function.
- `->`: Return type of the function.
- Last `type`: Return type of the function.

```go
(fn x [y, z: int] { } -> [int, bool]) // multiple parameters and returns
```

- `fn`: Keyword to define a function.
- `x`: Name of the function.
- `y`, `z`: Parameters of the function.
- `int`: Type of the parameters `y` and `z`.
- `{}`: Block of the function.
- `->`: Return type of the function.
- `int`, `bool`: Return types of the function.

This is a simple function that sums two numbers and returns the result.

```go
(fn sum [x: int, y: int] {
    (x + y)
} -> int)
```


## Conditionals

```go
(if (cond) {
    true 
} else { 
    false 
})
```

- `if`: Keyword to define a conditional.
- `cond`: Condition.
- `{}`: Block of the conditional.
- `true`: Value if the condition is true.
- `else`: Keyword to define the else block.
- `{}`: Block of the else block.
- `false`: Value if the condition is false.


```go
(if (cond) do true : false) // ternary operator
```

- `cond`: Condition.
- `?`: Operator to define the true block.
- `true`: Value if the condition is true.
- `:`: Operator to define the false block.
- `false`: Value if the condition is false.

More examples:

```go
// Function `even?`, returns true if the number is even, otherwise false.
(fn even? [x: int] {
    (if (x % 2 == 0) {
        true
    } else {
        false
    })
} -> bool)

// If the number is even, returns "yep!", otherwise "not even".
(if (even? x) { 
    "yep!"
} else {
    "not even"
})
```

This is a simple function that returns the maximum of two numbers and returns the result.

```go
(fn max [x, y: int] {
    (if (x > y) {
        x
    } else { 
        y 
    })
} -> int)
```
