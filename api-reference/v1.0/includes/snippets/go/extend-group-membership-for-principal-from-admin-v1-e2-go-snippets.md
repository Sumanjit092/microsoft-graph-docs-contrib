---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewPrivilegedAccessGroupEligibilityScheduleRequest()
accessId := graphmodels.MEMBER_PRIVILEGEDACCESSGROUPRELATIONSHIPS 
requestBody.SetAccessId(&accessId) 
principalId := "3cce9d87-3986-4f19-8335-7ed075408ca2"
requestBody.SetPrincipalId(&principalId) 
groupId := "2b5ed229-4072-478d-9504-a047ebd4b07d"
requestBody.SetGroupId(&groupId) 
action := graphmodels.ADMINEXTEND_SCHEDULEREQUESTACTIONS 
requestBody.SetAction(&action) 
scheduleInfo := graphmodels.NewRequestSchedule()
startDateTime , err := time.Parse(time.RFC3339, "2023-02-06T19:25:00.000Z")
scheduleInfo.SetStartDateTime(&startDateTime) 
expiration := graphmodels.NewExpirationPattern()
type := graphmodels.AFTERDATETIME_EXPIRATIONPATTERNTYPE 
expiration.SetType(&type) 
endDateTime , err := time.Parse(time.RFC3339, "2023-02-07T20:56:00.000Z")
expiration.SetEndDateTime(&endDateTime) 
scheduleInfo.SetExpiration(expiration)
requestBody.SetScheduleInfo(scheduleInfo)
justification := "Extend eligible request."
requestBody.SetJustification(&justification) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
eligibilityScheduleRequests, err := graphClient.IdentityGovernance().PrivilegedAccess().Group().EligibilityScheduleRequests().Post(context.Background(), requestBody, nil)


```