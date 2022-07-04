---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAlert()
additionalData := map[string]interface{}{


 := graphmodels.New()
assignedTo := "String"
.SetAssignedTo(&assignedTo) 
closedDateTime := "String (timestamp)"
.SetClosedDateTime(&closedDateTime) 
comments := []String {
	"String",

}
.SetComments(comments)
feedback := graphmodels.New()
"@odata.type" := "microsoft.graph.alertFeedback"
feedback.Set"@odata.type"(&"@odata.type") 
.SetFeedback(feedback)
id := "String (identifier)"
.SetId(&id) 
status := graphmodels.New()
"@odata.type" := "microsoft.graph.alertStatus"
status.Set"@odata.type"(&"@odata.type") 
.SetStatus(status)
tags := []String {
	"String",

}
.SetTags(tags)
vendorInformation := graphmodels.New()
provider := "String"
vendorInformation.SetProvider(&provider) 
vendor := "String"
vendorInformation.SetVendor(&vendor) 
.SetVendorInformation(vendorInformation)

	value := []graphmodels.Objectable {
		,

	}
}
requestBody.SetAdditionalData(additionalData)

graphClient.Security().AlertsById("alert-id").Post(requestBody)


```