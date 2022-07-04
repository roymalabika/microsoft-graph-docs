---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEducationSchool()
displayName := "String"
requestBody.SetDisplayName(&displayName) 
description := "String"
requestBody.SetDescription(&description) 
externalSource := graphmodels.STRING_EDUCATIONEXTERNALSOURCE 
requestBody.SetExternalSource(&externalSource) 
externalSourceDetail := "String"
requestBody.SetExternalSourceDetail(&externalSourceDetail) 
principalEmail := "String"
requestBody.SetPrincipalEmail(&principalEmail) 
principalName := "String"
requestBody.SetPrincipalName(&principalName) 
externalPrincipalId := "String"
requestBody.SetExternalPrincipalId(&externalPrincipalId) 
lowestGrade := "String"
requestBody.SetLowestGrade(&lowestGrade) 
highestGrade := "String"
requestBody.SetHighestGrade(&highestGrade) 
schoolNumber := "String"
requestBody.SetSchoolNumber(&schoolNumber) 
externalId := "String"
requestBody.SetExternalId(&externalId) 
phone := "String"
requestBody.SetPhone(&phone) 
fax := "String"
requestBody.SetFax(&fax) 
createdBy := graphmodels.NewIdentitySet()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.identitySet", 
}
createdBy.SetAdditionalData(additionalData)
requestBody.SetCreatedBy(createdBy)
address := graphmodels.NewPhysicalAddress()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.physicalAddress", 
}
address.SetAdditionalData(additionalData)
requestBody.SetAddress(address)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.educationSchool", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Education().Schools().Post(requestBody)


```