---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewIdentityProviderBase()
displayName := "Apple"
requestBody.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.socialIdentityProvider", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Identity().IdentityProvidersById("identityProviderBase-id").Patch(requestBody)


```