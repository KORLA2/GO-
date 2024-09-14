Like in any other programming language functions are used to avoid writing same piece of code over and over for small changes in code.

Like in Javascript in GO also we can return multiple values inside function.

## Declaration of Functions in Go

### Functions  which accepts nothing and returns nothing

```
func myfunction(){

fmt.Prinft("Hello iam a function);
}
```
### Functions  which accepts arguments and returns nothing
```
func myfunction(x string,y float64,z){
fmt.Prinft(x,y,z);

}
```
### Functions  which accepts arguments and returns something

```
func main(){
 x,y:=myfunction("hello",6.8,34)
}

func myfunction(x string,y float64,z) (string,float64){ // We have to specify what we are returning to the right side of the function definition
return x,y

}
```
##  Alternative way of returning
```
func main(){
 x,y:=myfunction()
}

func myfunction() (x string,y float64){   // By  Mentioning variable names here Go creates x,y variables redeclaring in function throws error .
x ="hello"
y =5.7
return; // We can simply write return here without specifying, Go looks what we are returing from the right side of the function.
}
```





