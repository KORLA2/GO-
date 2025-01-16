**integers (No Decimals )**
Sizes of these integers 

```
int  int8  int16  int32  int64
```

**Positive integers (No decimals )**

Sizes of these positive integers
```
uint uint8 uint16 uint32 uint64 uintptr
```

**Signed Decimal Numbers**
```
float32 float64
```

**Imaginary Numbers**

```
complex64 complex128
```

The size (8, 16, 32, 64, 128, etc) represents how many bits in memory will be used to store the variable. 
The "default" int and uint types refer to their respective 32 or 64-bit sizes depending on the architecture of the user's machine.

The "standard" sizes that should be used unless you have a specific performance need (e.g. using less memory) are:

int
uint
float64
complex128

**Converting Between Types**

x:=13.2
y:=int(x)


