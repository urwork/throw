# throw

```
package throw

func Throw(err error) {
	if err != nil {
		panic(err)
	}
}
```

Usage

```
package main

import (
	"io/ioutil"
	"os"

	. "github.com/urwork/throw"
)

func main() {
	filepath := "test.txt"

	_, err := os.Stat(filepath)
	Throw(err)

	Throw(ioutil.WriteFile(filepath, []byte("test"), 0644))

}
```


