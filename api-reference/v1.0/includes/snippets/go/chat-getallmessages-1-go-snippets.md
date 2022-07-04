---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.ChatRequestBuilderGetQueryParameters{
	Top: "2",
}
configuration := &graphconfig.ChatRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.UsersById("user-id").ChatsById("chat-id").GetWithRequestConfigurationAndResponseHandler(configuration, nil)


```