---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEducationClass()
displayName := "String"
requestBody.SetDisplayName(&displayName) 
mailNickname := "String"
requestBody.SetMailNickname(&mailNickname) 
description := "String"
requestBody.SetDescription(&description) 
createdBy := graphmodels.NewIdentitySet()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.identitySet", 
}
createdBy.SetAdditionalData(additionalData)
requestBody.SetCreatedBy(createdBy)
classCode := "String"
requestBody.SetClassCode(&classCode) 
externalName := "String"
requestBody.SetExternalName(&externalName) 
externalId := "String"
requestBody.SetExternalId(&externalId) 
externalSource := graphmodels.STRING_EDUCATIONEXTERNALSOURCE 
requestBody.SetExternalSource(&externalSource) 
externalSourceDetail := "String"
requestBody.SetExternalSourceDetail(&externalSourceDetail) 
grade := "String"
requestBody.SetGrade(&grade) 
term := graphmodels.NewEducationTerm()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.educationTerm", 
}
term.SetAdditionalData(additionalData)
requestBody.SetTerm(term)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.educationClass", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Education().Classes().Post(requestBody)


```