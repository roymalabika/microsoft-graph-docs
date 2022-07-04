---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewInternalSponsor()
additionalData := map[string]interface{}{
	"@odata.id" : "https://graph.microsoft.com/v1.0/users/{id}", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.IdentityGovernance().EntitlementManagement().ConnectedOrganizationsById("connectedOrganization-id").InternalSponsorsById("directoryObject-id").Post(requestBody)


```