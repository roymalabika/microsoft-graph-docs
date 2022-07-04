---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewIdentityProviderBase()
displayName := "contoso display name"
requestBody.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.samlOrWsFedExternalDomainFederation", 
	"issuerUri" : "https://contoso.com/issuerUri", 
	"metadataExchangeUri" : "https://contoso.com/metadataExchangeUri", 
	"passiveSignInUri" : "https://contoso.com/signin", 
	"preferredAuthenticationProtocol" : "wsFed", 


 := graphmodels.New()
"@odata.type" := "microsoft.graph.externalDomainName"
.Set"@odata.type"(&"@odata.type") 
id := "contoso.com"
.SetId(&id) 

	domains := []graphmodels.Objectable {
		,

	}
	"signingCertificate" : "MIIDADCCAeigAwIBAgIQEX41y8r6", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Directory().FederationConfigurations().Post(requestBody)


```