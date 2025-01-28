To know which type was passed to interface we use type switches.

```
type KGF{

  hero string
  age int

}
type Pushpa{

 herione string
 age int
} 

func main(){

  var i =interface{}
  i=Pushpa{"Rashmika","27"} Or i= KGF{"YASH",29} Both can be assigned as i is empty interface.

// How to check which type is assigned ? So we have type switches.


switch v:=i.(type){

case KGF:
fmt.Print(v.hero)

case Pushpa:
fmt.Print(v.herione)

default:

fmt.Print("None of the type")

}


}


```
