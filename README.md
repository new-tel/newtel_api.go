# New-Tel golang client 
A Golang client for communicating with the New-Tel API

## Features 

* CallPassword (Flash call).
* Request call.
* Autodial call.    

## Basic usage

To obtain the API_KEY and API_SIGNATURE 
please register here https://my.new-tel.net/register

```go
package main

import (
	"fmt"
	"log"
	
	"github.com/new-tel/newtel_api.go"
)

func main() {
	cfg := newtel_api.NewTelConfig{
		ApiKey:  "xxxxxxxxxxxxxx",
		ApiSign: "yyyyyyyyyyyyyyyyyyyyy",
	}
	client := newtel_api.NewTelClient(cfg)
	resp, err := client.CallPassword("+79081234567", "1234")
	if err != nil {
		log.Fatal(err)
	}
	fmt.Printf("%+v\n", resp)
}
```

## Documentation

RU documentation could be found 
[here](https://public.new-tel.net/docs/newtel_API.pdf)    

## Swagger link
https://swagger.new-tel.net/
