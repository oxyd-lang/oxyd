# Syntax

### Structure

## Variables

The structure of a variable is as follows:

```go
(var x: int)
```

```go
(var y: type = value)
```

More examples:

```go
(var x: int = 10)
```

```go
(var {
    x: float64 = 10.5,
    y: float64 = 14.4,
    z: float64 = 5.5
})
```

```go
(var {
    x: float64 = 10.5,
    y: int = 5,
    z: str = "oxyd"
})
```

- `var`: Keyword to define a variable.
- `x`: Name of the variable.
- `type`: Type of the variable.
- `=`: Assignment operator.
- `value`: Value of the variable.
- `{}` : Block of variables.

## Function

The structure of a function is as follows:

```go
(fn x [y: type, z: type] { } -> type)
```

- `fn`: Keyword to define a function.
- `x`: Name of the function.
- `y`, `z`: Parameters of the function.
- First and second `type`: Type of the parameters.
- `->`: Return type of the function.
- Last `type`: Return type of the function.

```go
(fn x [y, z: int] { } -> [int, bool]) // multiple parameters and returns
```

This is a simple function that sums two numbers and returns the result.

```go
(fn sum [x: int, y: int] {
    (x + y)
} -> int)
```


## Conditional

```go
(if (x) { } else { })
```

```go
(if (is_even x) { 
    "yep!"
} else {
    "not even"
})
```

- `if`: Keyword to define a conditional.
- `is_even`: Is a function that returns true if the number is even.
- `yep!`: Return value if the condition is true.
- `not even`: Return value if the condition is false.

```go
(fn x {
    (if (true) {
        true
    } else {
        false
    })
} -> bool)
```

This is a simple function that returns the maximum of two numbers and returns the result.

```go
(fn max [x: int, y: int] {
    (if (x > y) {
        x
    } else { 
        y 
    })
} -> int)
```
