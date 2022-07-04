---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewSendMailPostRequestBody()
message := graphmodels.NewMessage()
subject := "Project kickoff"
message.SetSubject(&subject) 


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
message.SetToRecipients(toRecipients)
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
message.SetAdditionalData(additionalData)
requestBody.SetMessage(message)

graphClient.Me().SendMail().Post(requestBody)


```