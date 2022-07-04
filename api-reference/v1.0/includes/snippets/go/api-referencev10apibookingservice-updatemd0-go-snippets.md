---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewBookingService()
defaultDuration := "PT30M"
requestBody.SetDefaultDuration(&defaultDuration) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.bookingService", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Solutions().BookingBusinessesById("bookingBusiness-id").ServicesById("bookingService-id").Patch(requestBody)


```