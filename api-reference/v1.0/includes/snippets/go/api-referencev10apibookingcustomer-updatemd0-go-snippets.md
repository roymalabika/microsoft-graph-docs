---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewBookingCustomerBase()
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.bookingCustomer", 
	"displayName" : "Adele", 
	"emailAddress" : "adele@relecloud.com", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Solutions().BookingBusinessesById("bookingBusiness-id").CustomersById("bookingCustomerBase-id").Patch(requestBody)


```