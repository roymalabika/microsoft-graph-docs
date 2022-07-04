---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewMessage()
subject := "Party planning"
requestBody.SetSubject(&subject) 


recipient := graphmodels.NewRecipient()
emailAddress := graphmodels.NewEmailAddress()
name := "Samantha Booth"
emailAddress.SetName(&name) 
address := "samanthab@contoso.onmicrosoft.com"
emailAddress.SetAddress(&address) 
recipient.SetEmailAddress(emailAddress)

toRecipients := []graphmodels.Recipientable {
	recipient,

}
requestBody.SetToRecipients(toRecipients)
additionalData := map[string]interface{}{


 := graphmodels.New()
mentioned := graphmodels.New()
name := "Dana Swope"
mentioned.SetName(&name) 
address := "danas@contoso.onmicrosoft.com"
mentioned.SetAddress(&address) 
.SetMentioned(mentioned)

	mentions := []graphmodels.Objectable {
		,

	}
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().Messages().Post(requestBody)


```