In Go, strings are just sequences of bytes: they can hold arbitrary data.
However, Go also has a special type, rune, which is an alias for int32. This means that a rune is a 32-bit integer, which is large enough to hold any Unicode code point.


When you need to work with individual characters in a string, you should use the rune type. 
It breaks strings up into their individual characters, which can be more than one byte long.
We can use zany characters like emojis and Chinese characters in our strings, and Go will handle them just fine.

EX:
```
const name = "bear"
	fmt.Printf("constant 'name' byte length: %d\n", len(name))
	fmt.Printf("constant 'name' rune length: %d\n", utf8.RuneCountInString(name))
```
Here both print statements prints 4 as length and rune count thats obvious.

But
```
const name = "🐻"
	fmt.Printf("constant 'name' byte length: %d\n", len(name))
	fmt.Printf("constant 'name' rune length: %d\n", utf8.RuneCountInString(name))
```

This prints 4 and 1 as, 1 rune size is 4 bytes and there is only one character in the string.
