The empty interface does not define any methods, so all types satisfy it. It's commonly used to handle values of any type, similar to Object in other languages.

```
func printAnything(value interface{}) {
    fmt.Println(value)
}

func main() {
    printAnything(42)
    printAnything("hello")
    printAnything(3.14)
}

```
