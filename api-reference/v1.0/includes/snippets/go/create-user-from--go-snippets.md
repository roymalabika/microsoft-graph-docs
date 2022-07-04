---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.New$refPostRequestBody()
additionalData := map[string]interface{}{
	"@odata.id" : "https://graph.microsoft.com/v1.0/users/{userId}", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Print().SharesById("printerShare-id").AllowedUsers().$ref().Post(requestBody)


```