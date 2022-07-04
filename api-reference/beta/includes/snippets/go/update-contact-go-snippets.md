---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewContact()


emailAddress := graphmodels.NewEmailAddress()
name := "Pavel Bansky"
emailAddress.SetName(&name) 
address := "pavelb@adatum.onmicrosoft.com"
emailAddress.SetAddress(&address) 
additionalData := map[string]interface{}{
	"type" : "personal", 
}
emailAddress.SetAdditionalData(additionalData)
emailAddress1 := graphmodels.NewEmailAddress()
address := "pavelb@fabrikam.onmicrosoft.com"
emailAddress1.SetAddress(&address) 
name := "Pavel Bansky"
emailAddress1.SetName(&name) 
additionalData := map[string]interface{}{
	"type" : "other", 
	"otherLabel" : "Volunteer work", 
}
emailAddress1.SetAdditionalData(additionalData)

emailAddresses := []graphmodels.EmailAddressable {
	emailAddress,
	emailAddress1,

}
requestBody.SetEmailAddresses(emailAddresses)

graphClient.Me().ContactsById("contact-id").Patch(requestBody)


```