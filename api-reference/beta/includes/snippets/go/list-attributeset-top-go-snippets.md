---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &graphconfig.AttributeSetsRequestBuilderGetQueryParameters{
	Top: 10,
}
configuration := &graphconfig.AttributeSetsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Directory().AttributeSets().GetWithRequestConfigurationAndResponseHandler(configuration, nil)


```