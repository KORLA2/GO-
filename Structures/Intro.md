We use structs in Go to represent structured data. 
It's often convenient to group different types of variables together. For example, if we want to represent a car we could do the following:

```
type car struct {
	brand      string
	model      string
	doors      int
	mileage    int
}

func main(){

var x = Movie {Rating :9.3,Name:"KGF"} // Initializing structure
fmt.Print(x.Name) // Prints Name

}
```

This creates a new struct type called car. All cars have a brand, model, doors and mileage.

Structs in Go are often used to represent data that you might use a dictionary or object in other languages.