---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewParticipant()
additionalData := map[string]interface{}{
	participants := []String {
		"",

	}
	"clientContext" : "clientContext-value", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Communications().CallsById("call-id").ParticipantsById("participant-id").Post(requestBody)


```