---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  "time"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewDeviceManagementExchangeConnector()
lastSyncDateTime , err := time.Parse(time.RFC3339, "2017-01-01T00:02:49.3205976-08:00")
requestBody.SetLastSyncDateTime(&lastSyncDateTime) 
status := graphmodels.CONNECTIONPENDING_DEVICEMANAGEMENTEXCHANGECONNECTORSTATUS 
requestBody.SetStatus(&status) 
primarySmtpAddress := "Primary Smtp Address value"
requestBody.SetPrimarySmtpAddress(&primarySmtpAddress) 
serverName := "Server Name value"
requestBody.SetServerName(&serverName) 
connectorServerName := "Connector Server Name value"
requestBody.SetConnectorServerName(&connectorServerName) 
exchangeConnectorType := graphmodels.HOSTED_DEVICEMANAGEMENTEXCHANGECONNECTORTYPE 
requestBody.SetExchangeConnectorType(&exchangeConnectorType) 
version := "Version value"
requestBody.SetVersion(&version) 
exchangeAlias := "Exchange Alias value"
requestBody.SetExchangeAlias(&exchangeAlias) 
exchangeOrganization := "Exchange Organization value"
requestBody.SetExchangeOrganization(&exchangeOrganization) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
exchangeConnectors, err := graphClient.DeviceManagement().ExchangeConnectors().ByDeviceManagementExchangeConnectorId("deviceManagementExchangeConnector-id").Patch(context.Background(), requestBody, nil)


```