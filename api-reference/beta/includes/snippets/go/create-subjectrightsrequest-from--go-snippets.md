---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewSubjectRightsRequest()
type := graphmodels.EXPORT_SUBJECTRIGHTSREQUESTTYPE 
requestBody.SetType(&type) 
dataSubjectType := graphmodels.CUSTOMER_DATASUBJECTTYPE 
requestBody.SetDataSubjectType(&dataSubjectType) 
displayName := "Export report for customer Id: 12345"
requestBody.SetDisplayName(&displayName) 
description := "This is a export request"
requestBody.SetDescription(&description) 
internalDueDateTime , err := time.Parse(time.RFC3339, "2022-07-20T22:42:28Z")
requestBody.SetInternalDueDateTime(&internalDueDateTime) 
dataSubject := graphmodels.NewDataSubject()
firstName := "Diego"
dataSubject.SetFirstName(&firstName) 
lastName := "Siciliani"
dataSubject.SetLastName(&lastName) 
email := "Diego.Siciliani@contoso.com"
dataSubject.SetEmail(&email) 
residency := "USA"
dataSubject.SetResidency(&residency) 
requestBody.SetDataSubject(dataSubject)
regulations := []String {
	"CCPA",

}
requestBody.SetRegulations(regulations)
additionalData := map[string]interface{}{
	"contentQuery" : "((\"Diego Siciliani\" OR \"Diego.Siciliani@contoso.com\") OR (participants:\"Diego.Siciliani@contoso.com\"))", 
	"externalId" : "F53BF2DA-607D-412A-B568-FAA0F023AC0B", 
	includeAllVersions := false
requestBody.SetIncludeAllVersions(&includeAllVersions) 
	includeAuthoredContent := true
requestBody.SetIncludeAuthoredContent(&includeAuthoredContent) 
	mailboxLocations := null
requestBody.SetMailboxLocations(&mailboxLocations) 
	pauseAfterEstimate := true
requestBody.SetPauseAfterEstimate(&pauseAfterEstimate) 
siteLocations := graphmodels.New()
"@odata.type" := "microsoft.graph.subjectRightsRequestAllSiteLocation"
siteLocations.Set"@odata.type"(&"@odata.type") 
	requestBody.SetSiteLocations(siteLocations)
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Privacy().SubjectRightsRequests().Post(requestBody)


```