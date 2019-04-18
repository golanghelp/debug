# golanghelp/debug

Dumps information about a golang variable. 

## Install

```bash
go get github.com/golanghelp/debug
```

## Demo

```golang
package main

import (
	. "github.com/golanghelp/debug"
)

func main() {
	D(123)

	D(3.14)

	D("abc")

	D(false)

	a := [3]int{1, 2, 3}
	D(a)

	b := make(map[string]int64)
	b["A"] = 1
	b["B"] = 2
	D(b)

	type Employee struct {
		ID        int
		Name      string
		Address   string
		Position  string
		Salary    int
		ManagerID int
	}
	var c Employee
	D(c)
}
```

Print:

```text
(int) 123
(float64) 3.14
(string) "abc"
(bool) false
([3]int)
  0(int) 1
  1(int) 2
  2(int) 3
(map[string]int64)
  A(int64) 1
  B(int64) 2
(main.Employee)
  ID(int) 0
  Name(string) ""
  Address(string) ""
  Position(string) ""
  Salary(int) 0
  ManagerID(int) 0
```
