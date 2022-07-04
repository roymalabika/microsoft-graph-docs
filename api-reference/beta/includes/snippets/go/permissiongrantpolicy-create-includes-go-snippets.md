---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewPermissionGrantConditionSet()
permissionType := graphmodels.DELEGATED_PERMISSIONTYPE 
requestBody.SetPermissionType(&permissionType) 
additionalData := map[string]interface{}{
	certifiedClientApplicationsOnly := true
requestBody.SetCertifiedClientApplicationsOnly(&certifiedClientApplicationsOnly) 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Policies().PermissionGrantPoliciesById("permissionGrantPolicy-id").Includes().Post(requestBody)


```