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


# Functions are just like values 

Functions are values too. They can be passed around just like other values.

Function values may be used as function arguments and return values.

```

func movie(st func(string)(string))(string){   // This movie function calls story function, if sentiment was yes then story return HIT and movie returns  Block Buster Movie
                                               // if any other parameter was passed as sentiment then stroy returns FLOP and movie returns FLOP Movie   

 if st("yes")=="HIT"{       
  return "Block Buster Movie"
 }

return "FLOP Movie" 
}

func main() {


 story:=func(sentiment string )(string){ // If a story has sentiment then this story function  returns HIT else FLOP 

     if sentiment=="yes" {  
      return "HIT"
     }

     return "FLOP"

   }

fmt.Print(movie(story))   // story function is passed to movie function. 

}
```



