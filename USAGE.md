<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	"log"
	"net/http"
	users "users/v3"
	"users/v3/pkg/models/shared"
)

func main() {
	s := users.New()

	ctx := context.Background()
	res, err := s.Pets.CreatePets(ctx, shared.Pet{
		ID:   596804,
		Name: "string",
	})
	if err != nil {
		log.Fatal(err)
	}

	if res.StatusCode == http.StatusOK {
		// handle response
	}
}

```
<!-- End SDK Example Usage [usage] -->