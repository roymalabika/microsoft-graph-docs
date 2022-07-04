---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewUser()
additionalData := map[string]interface{}{
	"password" : "1234567890", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.UsersById("user-id").Post(requestBody)


```