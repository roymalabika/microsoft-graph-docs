---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewConversationMember()
roles := []String {
	"owner",

}
requestBody.SetRoles(roles)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.aadUserConversationMember", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.TeamsById("team-id").MembersById("conversationMember-id").Patch(requestBody)


```