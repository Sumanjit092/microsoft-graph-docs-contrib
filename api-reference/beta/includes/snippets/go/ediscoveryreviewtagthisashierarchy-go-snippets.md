---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  //other-imports
)


// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
microsoftGraphSecurityAsHierarchy, err := graphClient.Security().Cases().EdiscoveryCases().ByEdiscoveryCaseId("ediscoveryCase-id").Tags().MicrosoftGraphSecurityAsHierarchy().GetAsAsHierarchyGetResponse(context.Background(), nil)


```