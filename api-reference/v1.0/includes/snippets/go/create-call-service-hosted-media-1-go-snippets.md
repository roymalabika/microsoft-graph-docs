---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewCall()
callbackUri := "https://bot.contoso.com/callback"
requestBody.SetCallbackUri(&callbackUri) 


invitationParticipantInfo := graphmodels.NewInvitationParticipantInfo()
identity := graphmodels.NewIdentitySet()
user := graphmodels.NewIdentity()
displayName := "John"
user.SetDisplayName(&displayName) 
id := "112f7296-5fa4-42ca-bae8-6a692b15d4b8"
user.SetId(&id) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.identity", 
}
user.SetAdditionalData(additionalData)
identity.SetUser(user)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.identitySet", 
}
identity.SetAdditionalData(additionalData)
invitationParticipantInfo.SetIdentity(identity)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.invitationParticipantInfo", 
}
invitationParticipantInfo.SetAdditionalData(additionalData)

targets := []graphmodels.InvitationParticipantInfoable {
	invitationParticipantInfo,

}
requestBody.SetTargets(targets)
requestedModalities := []graphmodels.Modalityable {
	"audio",

}
requestBody.SetRequestedModalities(requestedModalities)
mediaConfig := graphmodels.NewMediaConfig()
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.serviceHostedMediaConfig", 
}
mediaConfig.SetAdditionalData(additionalData)
requestBody.SetMediaConfig(mediaConfig)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.call", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Communications().Calls().Post(requestBody)


```