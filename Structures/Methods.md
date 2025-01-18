While Go is not object-oriented, it does support methods that can be defined on structs.
Methods are just functions that have a receiver. A receiver is a special parameter that syntactically goes before the name of the function.

```
type Movie struct {
	Rating float64
	Name   string
	Hero
}
//mo is a placeholder, it is the object through which this function is called.

func (mo Movie) help() int {

	return int(mo.Rating)
}

type Hero struct {
	age  int
	name string
}

func main() {

	x := Movie{Rating: 9.8,
		Name: "KGF"}
	fmt.Println(x.help())

}
```
