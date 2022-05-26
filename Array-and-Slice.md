# Array and Slice  <a name="arrayandslice"></a>

Table of Contents  

1. [Array](#Array)
2. [Slice](#Slice)
3. [Examples](#Examples)

## Array <a name="Array"></a>  

Array is static.  
Array is messy.  
Use slice instead.  

[Back to top](#arrayandslice)  

## Slice <a name="Slice"></a>

Slice is a window of an array.   

Slice is flexible.  

Slice is a struct contains 3 things:
- Pointer to the array
- Length
- Capacity

[Back to top](#arrayandslice)  

## Examples <a name="Examples"></a>

Passing Slice to Function

```
package main
import (
  "fmt"
)

func foo(my_slice []int) bool {
  my_slice[0] = my_slice[0] + 1   // increment only 1st argument
  return true
}

func main() {
  a := []int{1, 2, 3}   // declaring slice without giving the length
  if foo(a) {
    fmt.Println(a)  // getting output [2 2 3]
  }
}

```

[Back to top](#arrayandslice)  
