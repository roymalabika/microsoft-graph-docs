---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAttachment()
name := "name-value"
requestBody.SetName(&name) 
additionalData := map[string]interface{}{
	"@odata.type" : "#Microsoft.OutlookServices.ItemAttachment", 
item := graphmodels.New()
"@odata.type" := "microsoft.graph.message"
item.Set"@odata.type"(&"@odata.type") 
	requestBody.SetItem(item)
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().EventsById("event-id").Attachments().Post(requestBody)


```