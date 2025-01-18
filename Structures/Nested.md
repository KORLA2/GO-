
**Nested Structs in Go**

Structs can be nested to represent more complex entities:

```
type Movie struct {

Rating float64
Name string
Hero Brand
}

type Brand struct {
 Age int
 Name string
}

func main(){

var x = Movie {Rating :9.3,Name:"KGF"} // Initializing structure or can also be initialized with x:= 
fmt.Print(x.Name) // Prints Name

}

```
