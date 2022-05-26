# Pointer * and Address &  <a name="pointandaddress"></a>

Table of Contents  

1. [Ampersand](#Ampersand)  
2. [Asterisk](#Asterisk)  
3. [Examples](#Examples)  

## Ampersand  <a name="Ampersand"></a>

Keyboard key = &  

Only 1 meaning in golang:  
- memory address location of a variable  

[Back to top](#pointandaddress)  


## Asterisk  <a name="Asterisk"></a>

Keyboard key = *  

2 meanings in golang:  
- Noun: Pointer variable declaration for storing memory address/container location
- Verb: Dereferencing operator which represents the content value of the pointer variable

[Back to top](#pointandaddress)  

## Examples  <a name="Examples"></a>

Variable Declaration and Dereferencing

```
var x int = 10  # first declare x = 10
var y *int = &x   # now y stores the address of x but not 10
fmt.Println("y = ", y)  # will get address liked y = 0000123
fmt.Println("*y = ", *y)  # will get content liked *y = 10
```

Call by Reference

```
package main
import (
  "fmt"
)

func addition(y *int) (int, int) {
  z := 0
  *y = *y + 1                 // Dereferencing as I want the content value to do something
  return *y, z                // Returning the content values
}


func main() {
  var x int = 10
  fmt.Println(addition(&x))   // Passing in address of x; then gives output 11 0
  fmt.Println(x)              // x is incremented as my wish; 11
}

```

[Back to top](#pointandaddress)  
