# Basic output
di dalam kode kode sebelumnya, kita menggunakan package `fmt` (format) yang digunakan sebagai I/O agar muncul output pada terminal. salah satu fungsi yang dipakai adalah `Println`

## fmt.Println

`fmt.Println()` "Print line" merupakan fungsi yang sering dipakai untuk menampilkan output. fungsi ini akan menampilkan output dengan menambah newline dibelakangnya, sehingga output berikutnya akan muncul dibaris baru. selain dalam bentuk string, tipe data integer & boolean juga bisa dicetak, & dalam satu syntax bisa berisi lebih dari 1 data.
```go
package main

import "fmt"

func main() {
	fmt.Println("hello")
	fmt.Println(1234)
	fmt.Println(True)
}
```

```
$ go run main.go
//output
hello 
1234 
True
```

## fmt.print
`fmt.Print()` "Print" berfungsi mencetak tanpa membuat baris baru, berbeda dengan `Println` yang mencetak sekaligus membuat baris baru.

```go
package main

import "fmt"

func main() {
	fmt.Println("hello")
	fmt.Println(1234)
	fmt.Println(True)
}
```

## fmt.printf
The `fmt.Printf()` "Printffunction in Go language formats according to a format specifier and writes to standard output. Moreover, this function is defined under the fmt package. Here, you need to import the “fmt” package in order to use these functions.

**Syntax:** 

func Printf(format string, a ...interface{}) (n int, err error)

**Parameters:** This function accepts two parameters which are illustrated below: 

-   **format string:** This contains some strings along with some verbs.
-   **a …interface{}:** This contains specified constant variables.

**Return Value:** It returns the number of bytes written and any write error encountered.


untuk karakter konversi bisa dilihat di [sini](https://www.geeksforgeeks.org/fmt-printf-function-in-golang-with-examples/)

```go
// Golang program to illustrate the usage of
// fmt.Printf() function

// Including the main package
package main

// Importing fmt
import (
	"fmt"
)

// Calling main
func main() {
	// Declaring some const variables
	const name, dept = "GeeksforGeeks", "CS"
	const num1, num2, num3 = 5, 10, 15

	// Calling Printf() function
	fmt.Printf("%s is a %s Portal.\n", name, dept)
	// It is conventional not to worry about any
	// error returned by Printf.

	// Declaring some const variables
	const name, dept = "GeeksforGeeks", "CS"

	// Calling Printf() function
	fmt.Printf("%s is a %s Portal.\n", name, dept)
	fmt.Printf("%d + %d = %d\n", num1, num2, num3)

	// It is conventional not to worry about any
	// error returned by Printf.
}
```
```output
GeeksforGeeks is a CS portal.
5 + 10 = 15
```
