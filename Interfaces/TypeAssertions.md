A type assertion provides access to an interface value's underlying concrete value.

t := i.(T)
This statement asserts that the interface value i holds the concrete type T and assigns the underlying T value to the variable t.

If i does not hold a T, the statement will trigger a panic.

To test whether an interface value holds a specific type, a type assertion can return two values: the underlying value and a boolean value that reports whether the assertion succeeded.

t, ok := i.(T)
If i holds a T, then t will be the underlying value and ok will be true.

If not, ok will be false and t will be the zero value of type T, and no panic occurs.

```

type Movie interface{

}

type KGF struct {
  hero string
  age int
}
func main(){

var m Movie =KGF{"Yash",29}

m.hero ❌ You cant access underlying value

val,ok:=m.(KGF) val holds KGF instance ok holda true

val.hero ✅

}

```

