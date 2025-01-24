Interfaces are just collections of method signatures that a type must implement. 

An interface is defined using the interface keyword. It specifies a set of methods that a type must implement to satisfy the interface.

```
type Movie interface {
      Story() bool
      Sentiment() bool
  }
    
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
