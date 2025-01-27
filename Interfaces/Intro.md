Interfaces are just collections of method signatures that a type must implement. 

An interface is defined using the interface keyword. It specifies a set of methods that a type must implement to satisfy the interface.

```
type Movie interface {
      Story() bool
      Sentiment() bool
  }
A type satisfies an interface if it implements all the methods defined in the interface. There's no need to explicitly declare that a type implements an interface
    type KGF struct {
    hero string 
    }

        func (K KGF) Story() bool{
        return true;
        
        }
        func (K KGF) Sentiment() bool{
        return true;
        
        }
    type Pushpa struct {
        hero string 
    }
        func (P Pushpa) Story() bool{
        return true;
        
        }
        func (P Pushpa) Sentiment() bool{
        return true;
        
        }
```

// Interfaces can hold any value that implements the methods required by the interface.
```
func main(){

k:=KGF{hero:"Yash"}
var m Movie=k // Correct as type KGF implements Movie  
fmt.Print(m.Story());

}
```



