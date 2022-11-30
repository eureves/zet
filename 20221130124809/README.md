# Using for loop in Go

Go `for` loops are much like C but little more generalized. 

For example there are no `do-while`. Instead there are three forms of `for` loops.

```go 
// Like a C for
for init; condition; post { }

// Like a C while
for condition { }

// Like a C for(;;)
for { }
```

Also since `i++` is not an expression but a statement, multiple variables should use parallel assignment in init and past blocks of `for` loops.

```go 
for i, j := 0, len(a)-1; i < j; i, j = i+1, j-1 {
    a[i], a[j] = a[j], a[i]
}
```

#go #basics