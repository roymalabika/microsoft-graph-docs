---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewManagedDevice()
additionalData := map[string]interface{}{
	managedDeviceIds := []String {
		"30d0e128-de93-41dc-89ec-33d84bb662a0",
		"7c82a3e3-9459-44e4-94d9-b92f93bf78dd",

	}
	"restorePointDateTime" : "2021-09-23T04:00:00.0000000", 
	"timeRange" : "before", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.DeviceManagement().ManagedDevicesById("managedDevice-id").Post(requestBody)


```