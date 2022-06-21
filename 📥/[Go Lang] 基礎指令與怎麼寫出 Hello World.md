## Go 官方文件
[連結](https://go.dev/doc/#learning)

---
## Coding Command
### Import
* 保留字
* Access other packages
* Go std. library includes many packages e.g. "fmt"
* Search GOROOT and GOPATH
---
### go build
* Compile the program
* Compile an main package, same name as the .go file
---
### go doc
* Print documentation for a package
---
### go fm2t
* Formats source code files
---
### go get
* Downloads the package an installs them
---
### go lists
* Listed all package that installed
---
### go run
* Compiles .go files and runs 
---
### go test
* Runs tests using files ending in "_test.go_"
---
## Variables
### Namining 
* Start with a letters
* Any number of letters, digits, underscores
* Case sensitive
* Don't use keywords
---
### Variables
* Data storage
* name + type
* Must have declarations
```Go = 
var x int
```
* Declare more at same time
```Go=
var x, y int
```
* Integer, Operator, Floating same as Java
---
### String
* Byte (character) sequences
---
## Variable Declarations
* Defining an alias for a type
* May improve clarity
	* `type Celsius float64`
	* `type IDnum int`
* Can declare variables using the type alias
	* `var temp Celsius`
	* `var pid IDnum`
### Initializing Variables
* Initialize in the declaration
	* `var x  int = 100`
	* `var x = 100`
		* 但有時候會推斷出你不想要的
* Uninitialized variables have a zero value
	* `var x int // x=0`
	* `var x string // x = ""`
### Short Variable Declarations
* Can perform a declaration and initialization together with `:=`
```go=
x:=100
```
* Variable is declared as type of expression on the right hand side
* Can only do this inside a function
## Hello World!
### 打開 VS Code，安裝 Go Lang 插件
![[截圖 2022-06-13 01.07.46.png]]
### 創建新檔案並寫下
```Go=
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}

```
### 透過 terminal 執行 `go run`
![[截圖 2022-06-13 01.09.34.png]]
