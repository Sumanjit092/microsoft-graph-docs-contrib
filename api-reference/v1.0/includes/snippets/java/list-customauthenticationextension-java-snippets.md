---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

// Code snippets are only available for the latest version. Current version is 6.x

GraphServiceClient graphClient = new GraphServiceClient(requestAdapter);

CustomAuthenticationExtensionCollectionResponse result = graphClient.identity().customAuthenticationExtensions().get(requestConfiguration -> {
	requestConfiguration.queryParameters.filter = "isOf('microsoft.graph.onTokenIssuanceStartCustomExtension')";
});


```