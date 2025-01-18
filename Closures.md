A closure is a function that references variables from outside its own function body. The function may access and assign to the referenced variables.

Example:

```
func adder() func(int) int {
sum:=0;
	return func( sum1 int) int{
		sum +=sum1;
		return sum
	}
}


func main(){

returned:= adder()
returned(2);
sum:=returned(3);
fmt.Print(sum) // Prints 5
}


```
