---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.ListItemRequestBuilderGetQueryParameters{
	Token: "1230919asd190410jlka",
}
configuration := &graphconfig.ListItemRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.SitesById("site-id").ListsById("list-id").ItemsById("listItem-id").GetWithRequestConfigurationAndResponseHandler(configuration, nil)


```