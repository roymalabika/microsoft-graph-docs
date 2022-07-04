---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewChannel()
membershipType := graphmodels.PRIVATE_CHANNELMEMBERSHIPTYPE 
requestBody.SetMembershipType(&membershipType) 
displayName := "My First Private Channel"
requestBody.SetDisplayName(&displayName) 
description := "This is my first private channels"
requestBody.SetDescription(&description) 


conversationMember := graphmodels.NewConversationMember()
roles := []String {
	"owner",

}
conversationMember.SetRoles(roles)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.aadUserConversationMember", 
	"user@odata.bind" : "https://graph.microsoft.com/v1.0/users('jacob@contoso.com')", 
}
conversationMember.SetAdditionalData(additionalData)

members := []graphmodels.ConversationMemberable {
	conversationMember,

}
requestBody.SetMembers(members)
additionalData := map[string]interface{}{
	"@odata.type" : "#Microsoft.Graph.channel", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.TeamsById("team-id").Channels().Post(requestBody)


```