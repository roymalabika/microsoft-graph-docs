---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewGroupLifecyclePolicie()
additionalData := map[string]interface{}{
	"groupId" : "ffffffff-ffff-ffff-ffff-ffffffffffff", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.GroupLifecyclePoliciesById("groupLifecyclePolicy-id").Post(requestBody)


```