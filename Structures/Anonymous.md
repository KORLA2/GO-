**Anonymous Structs**

An anonymous struct is just like a normal struct, but it is defined without a name and therefore cannot be referenced elsewhere in the code.

To create an anonymous struct, just instantiate the instance immediately using a second pair of brackets after declaring the type:

```
myCar := struct {
  brand string
  model string
} {
  brand: "tesla",
  model: "model 3"
}
```

**Nesting Anonymous structures with in structure**
```
type Engine struct {
    Horsepower int
    Type       string
}

type Car struct {
    Make   string
    Model  string
    Engine Engine // Nested struct
}

func main() {
    myCar := Car{
        Make:  "Toyota",
        Model: "Camry",
        Engine: Engine{
            Horsepower: 200,
            Type:       "Petrol",
        },
    }

    // Accessing fields
    fmt.Println("Engine Type:", myCar.Engine.Type) // Must prefix with `Engine`
}

```

**Embedded Structs**

```
type Engine struct {
    Horsepower int
    Type       string
}

type Car struct {
    Make   string
    Model  string
    Engine // Embedded struct
}
func main() {
    myCar := Car{
        Make:  "Toyota",
        Model: "Camry",
        Engine: Engine{
            Horsepower: 200,
            Type: "Petrol",
        },
    }

    // Accessing fields directly
    fmt.Println("Engine Type:", myCar.Type)        // No need to prefix with `Engine`
    fmt.Println("Horsepower:", myCar.Horsepower)   // Directly accessible
}

```

