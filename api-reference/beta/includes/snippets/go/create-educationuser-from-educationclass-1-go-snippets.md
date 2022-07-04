---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.New$refPostRequestBody()
additionalData := map[string]interface{}{
	"@odata.id" : "https://graph.microsoft.com/beta/education/users/13015", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Education().ClassesById("educationClass-id").Members().$ref().Post(requestBody)


```