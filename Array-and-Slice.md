# Array and Slice

## Array

Array is static.  
Array is messy.  
Use slice instead.  


## Slice

Slice is a window of an array.   

Slice is flexible.  

Slice is a struct contains 3 things:
- Pointer to the array
- Length
- Capacity



## Examples

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
