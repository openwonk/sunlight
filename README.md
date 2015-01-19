Sunlight Congress API Client
===================

Library provides access to the [Sunlight Foundation's US Congress API](https://sunlightlabs.github.io/congress).  
*This service requires a [registration key](http://sunlightfoundation.com/api/accounts/register).*

###Usage
```go
package main

import (
	bank "github.com/openwonk/worldbank"
	"fmt"
)

func main() {
	s := bank.Series{
		Language: "en",

		Countries: []string{
			"bra",
			"chn",
		},
		Indicators: []string{
			"SP.POP.TOTL",
		},
		Start:     bank.Date{Year: "2011", Subunit: "Q2"},
		End:       bank.Date{Year: "2013", Subunit: "Q4"},
		Format:    "json",
		Frequency: "Q",
	}

	s.Querify()
	s.Request()
	s.Write("test.json")
	s.Reset()
	fmt.Println(s)

}
```
<br>
<br>

<hr>
<small>
<strong>OpenWonk &copy; 2015 MIT License</strong>
</small>

