---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewMailFolder()
displayName := "Weekly digests"
requestBody.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.mailSearchFolder", 
	includeNestedFolders := true
requestBody.SetIncludeNestedFolders(&includeNestedFolders) 
	sourceFolderIds := []String {
		"AQMkADYAAAIBDAAAAA==",

	}
	"filterQuery" : "contains(subject, 'weekly digest')", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().MailFoldersById("mailFolder-id").ChildFolders().Post(requestBody)


```