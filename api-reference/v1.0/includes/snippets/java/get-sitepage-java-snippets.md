---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

// Code snippets are only available for the latest version. Current version is 6.x

GraphServiceClient graphClient = new GraphServiceClient(requestAdapter);

SitePage result = graphClient.sites().bySiteId("{site-id}").pages().byBaseSitePageId("{baseSitePage-id}").graphSitePage().get(requestConfiguration -> {
	requestConfiguration.queryParameters.select = new String []{"id", "name"};
});


```