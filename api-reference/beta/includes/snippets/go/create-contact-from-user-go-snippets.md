---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewContact()
givenName := "Pavel"
requestBody.SetGivenName(&givenName) 
surname := "Bansky"
requestBody.SetSurname(&surname) 


emailAddress := graphmodels.NewEmailAddress()
address := "pavelb@contoso.onmicrosoft.com"
emailAddress.SetAddress(&address) 
name := "Pavel Bansky"
emailAddress.SetName(&name) 
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
additionalData := map[string]interface{}{


 := graphmodels.New()
number := "+1 732 555 0102"
.SetNumber(&number) 
type := "business"
.SetType(&type) 

	phones := []graphmodels.Objectable {
		,

	}
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().Contacts().Post(requestBody)


```