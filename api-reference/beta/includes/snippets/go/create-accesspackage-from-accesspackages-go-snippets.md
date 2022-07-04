---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAccessPackage()
displayName := "sales reps"
requestBody.SetDisplayName(&displayName) 
description := "outside sales representatives"
requestBody.SetDescription(&description) 
additionalData := map[string]interface{}{
	"catalogId" : "aa2f6514-3232-46e7-a08a-2411ad8d7128", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.IdentityGovernance().EntitlementManagement().AccessPackages().Post(requestBody)


```