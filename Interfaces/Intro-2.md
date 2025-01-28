
```
type Movie interface{

  Story()

}

type KGF struct{

 hero string
 age int
}

func (K *KGF) Story(){   // Now we say KGF type implements Movie only if address of KGF instance is passed to interface instance.

 K.age=28; 

}
func main(){

var k = KGF{"Yash",32}
var m Movie = &k  ✅;
m = k ❌ as KGF implements Movie, Story function expects a pointer receiver to implement Movie type but we are passing value.

}

```
