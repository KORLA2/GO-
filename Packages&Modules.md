
## Package

 1. A package is a way to group related Go files together.
 2. Every Go file belongs to a package, and a package is essentially a directory containing one or more Go source files.
 3. A package can contain functions, types, variables, constants, and other packages.
 4.  Packages can be imported into other Go programs, allowing us to reuse code.
 5. For example, the fmt package contains formatting functions like Println

## Modules
1. A module is a collection of related Go packages that are versioned together and distributed.
2.Modules are used to manage dependencies in Go programs.
3.The module system was introduced in Go 1.11 to make it easier to manage versions of your code and its dependencies.
4.Modules are defined by a go.mod file, which declares the module's name and its dependencies.

### Splitting Code accross Files

This is very simple in go both files must belog to same package and we can use functions, types, variables, constants from one file in other.

```
Hello.go
----------
package main
import ("fmt")

func main(){
fmt.Println(name()) // Name function is from other file
}
```
```
package main
import ("fmt")

func name() (string){
return "Goutham"
}
```

### Splitting Code accross Packages

For this we need to have a module :
```
go mod init calculator

```
This initiates Module called calculator.

If we want to create our own package for example maths and use this package in our file then this file must be inside maths(name of the package) folder.

For Example this how the basic file structure looks like:
```
calculator/
    go.mod
    math/
        add.go
    main.go
```
  ```
 add.go
-----------
package math

// Add adds two integers.
func Add(a, b int) int {
    return a + b
}
 ```

```
main.go
---------
package main

import (
    "fmt"
    "calculator/math" 
)

func main() {
    result := math.Add(3, 4)
    fmt.Println(result)  // Output: 7
}
```
 
 
