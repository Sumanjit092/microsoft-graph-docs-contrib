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

requestBody := graphmodels.NewBookingCustomerBase()
displayName := "Joni Sherman"
requestBody.SetDisplayName(&displayName) 
emailAddress := "jonis@relecloud.com"
requestBody.SetEmailAddress(&emailAddress) 


physicalAddress := graphmodels.NewPhysicalAddress()
street := "4567 Main Street"
physicalAddress.SetStreet(&street) 
city := "Buffalo"
physicalAddress.SetCity(&city) 
state := "NY"
physicalAddress.SetState(&state) 
countryOrRegion := "USA"
physicalAddress.SetCountryOrRegion(&countryOrRegion) 
postalCode := "98052"
physicalAddress.SetPostalCode(&postalCode) 
additionalData := map[string]interface{}{
	"postOfficeBox" : "", 
	"type" : "home", 
}
physicalAddress.SetAdditionalData(additionalData)
physicalAddress1 := graphmodels.NewPhysicalAddress()
street := "4570 Main Street"
physicalAddress1.SetStreet(&street) 
city := "Buffalo"
physicalAddress1.SetCity(&city) 
state := "NY"
physicalAddress1.SetState(&state) 
countryOrRegion := "USA"
physicalAddress1.SetCountryOrRegion(&countryOrRegion) 
postalCode := "98054"
physicalAddress1.SetPostalCode(&postalCode) 
additionalData := map[string]interface{}{
	"postOfficeBox" : "", 
	"type" : "business", 
}
physicalAddress1.SetAdditionalData(additionalData)

addresses := []graphmodels.PhysicalAddressable {
	physicalAddress,
	physicalAddress1,
}
requestBody.SetAddresses(addresses)


phone := graphmodels.NewPhone()
number := "206-555-0100"
phone.SetNumber(&number) 
type := graphmodels.HOME_PHONETYPE 
phone.SetType(&type) 
phone1 := graphmodels.NewPhone()
number := "206-555-0200"
phone1.SetNumber(&number) 
type := graphmodels.BUSINESS_PHONETYPE 
phone1.SetType(&type) 

phones := []graphmodels.Phoneable {
	phone,
	phone1,
}
requestBody.SetPhones(phones)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
customers, err := graphClient.Solutions().BookingBusinesses().ByBookingBusinessId("bookingBusiness-id").Customers().Post(context.Background(), requestBody, nil)


```