
# openai-go

This [SDK](https://github.com/sdk-fabric/openai-go) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/openai

## Usage

```go
import (
	"github.com/sdk-fabric/openai-go/sdk"
)

var client, _ = sdk.Build("[access_token]");

// Creates a model response for the given chat conversation.
response, err := client.Completions().Create(CompletionRequest{})

// Delete a stored chat completion.
response, err := client.Completions().Delete("completion_id")

// List stored Chat Completions.
response, err := client.Completions().Getall("after", 1, "model", "order")

// Creates a model response.
response, err := client.Responses().Create(ResponseRequest{})
```
