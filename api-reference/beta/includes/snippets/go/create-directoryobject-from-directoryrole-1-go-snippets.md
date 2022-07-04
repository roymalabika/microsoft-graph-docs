---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.New$refPostRequestBody()
additionalData := map[string]interface{}{
	"@odata.id" : "https://graph.microsoft.com/beta/users/0f933635-5b77-4cf4-a577-f78a5eb090a2", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.DirectoryRolesById("directoryRole-id").Members().$ref().Post(requestBody)


```