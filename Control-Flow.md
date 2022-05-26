# Control Flow <a name="controlflow"></a>

TOC   

1. [If Else](#ifelse)  
2. [For Loop](#forloop)  
3. [Switch case](#switchcase)  

## If Else <a name="ifelse"></a>

Syntax

```
if <condition> {
  <consequent>
} else if <condition> {
  <consequent>
} else {
  <consequent>
}
```

Example

```
if x > 5 {
  fmt.Printf( "%d is greater than 5.\n", x )
} else if x < 5 {
  fmt.Printf( "%d is less than 5.\n", x )
} else {
  fmt.Printf( "%d is equal to 5.\n", x )
}
```

[Back to top](#controlflow)  


## For loop <a name="forloop"></a>

Syntax

```
// 1. Typical for loop
for <init>; <cond>; <update> {
  <stmts>
}

// 2. While loop
for <cond> {
  <stmts>
  <update>
}

// 3. infinte While loop, always use with break
for {
  <conds>
  <update>
}
```

Example

```
// 1. Typical for loop
for i := 0; i < 3; i++ {
  fmt.Println( "everything" )
}

// 2. While loop
j := 0
for j < 3 {
  fmt.Println( "condition only" )
  j++
}

// 3. infinte While loop, always use with break
k := 0
for {
  if k >= 6 { break } // break out of loop at iteration 4
  k++
  if k == 3 { continue } // skip printing
  fmt.Println( "k =", k )
}
```

[Back to top](#controlflow)  

## Switch case <a name="switchcase"></a>

Syntax

```
// tag with 1 variable
switch <variable> {
  case <value>:
    <stmts>
  default:
    <stmts>
}

// tagless, multiple variables
switch {
  case <cond1>:
    <stmts>
  case <cond2>:
    <stmts>
  default:
    <stmts>
}

```

Example

```
a := "hello"
switch a {
  case "hello":
    fmt.Println( "x = hello" )
  case "world":
    fmt.Println( "x = world" )
  default:
    fmt.Println( "x is not equal to hello or world" )
}

b := 0
c := 5
switch {
  case b > 1:
    fmt.Println( "case 1" )
  case c > 3:
    fmt.Println( "case 2" )
  default:
    fmt.Println( "no case" )
}
```

[Back to top](#controlflow)  
