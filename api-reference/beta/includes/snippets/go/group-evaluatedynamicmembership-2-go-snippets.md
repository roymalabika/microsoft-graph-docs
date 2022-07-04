---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewGroup()
additionalData := map[string]interface{}{
	"memberId" : "319b41e8-d9e4-42f8-bdc9-741113f48b33", 
	"membershipRule" : "(user.displayName -startsWith \"EndTestUser\")", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.GroupsById("group-id").Post(requestBody)


```