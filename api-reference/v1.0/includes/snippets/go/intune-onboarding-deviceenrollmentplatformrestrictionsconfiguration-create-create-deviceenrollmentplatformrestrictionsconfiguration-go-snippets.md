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

requestBody := graphmodels.NewDeviceEnrollmentConfiguration()
displayName := "Display Name value"
requestBody.SetDisplayName(&displayName) 
description := "Description value"
requestBody.SetDescription(&description) 
priority := int32(8)
requestBody.SetPriority(&priority) 
version := int32(7)
requestBody.SetVersion(&version) 
iosRestriction := graphmodels.NewDeviceEnrollmentPlatformRestriction()
platformBlocked := true
iosRestriction.SetPlatformBlocked(&platformBlocked) 
personalDeviceEnrollmentBlocked := true
iosRestriction.SetPersonalDeviceEnrollmentBlocked(&personalDeviceEnrollmentBlocked) 
osMinimumVersion := "Os Minimum Version value"
iosRestriction.SetOsMinimumVersion(&osMinimumVersion) 
osMaximumVersion := "Os Maximum Version value"
iosRestriction.SetOsMaximumVersion(&osMaximumVersion) 
requestBody.SetIosRestriction(iosRestriction)
windowsRestriction := graphmodels.NewDeviceEnrollmentPlatformRestriction()
platformBlocked := true
windowsRestriction.SetPlatformBlocked(&platformBlocked) 
personalDeviceEnrollmentBlocked := true
windowsRestriction.SetPersonalDeviceEnrollmentBlocked(&personalDeviceEnrollmentBlocked) 
osMinimumVersion := "Os Minimum Version value"
windowsRestriction.SetOsMinimumVersion(&osMinimumVersion) 
osMaximumVersion := "Os Maximum Version value"
windowsRestriction.SetOsMaximumVersion(&osMaximumVersion) 
requestBody.SetWindowsRestriction(windowsRestriction)
windowsMobileRestriction := graphmodels.NewDeviceEnrollmentPlatformRestriction()
platformBlocked := true
windowsMobileRestriction.SetPlatformBlocked(&platformBlocked) 
personalDeviceEnrollmentBlocked := true
windowsMobileRestriction.SetPersonalDeviceEnrollmentBlocked(&personalDeviceEnrollmentBlocked) 
osMinimumVersion := "Os Minimum Version value"
windowsMobileRestriction.SetOsMinimumVersion(&osMinimumVersion) 
osMaximumVersion := "Os Maximum Version value"
windowsMobileRestriction.SetOsMaximumVersion(&osMaximumVersion) 
requestBody.SetWindowsMobileRestriction(windowsMobileRestriction)
androidRestriction := graphmodels.NewDeviceEnrollmentPlatformRestriction()
platformBlocked := true
androidRestriction.SetPlatformBlocked(&platformBlocked) 
personalDeviceEnrollmentBlocked := true
androidRestriction.SetPersonalDeviceEnrollmentBlocked(&personalDeviceEnrollmentBlocked) 
osMinimumVersion := "Os Minimum Version value"
androidRestriction.SetOsMinimumVersion(&osMinimumVersion) 
osMaximumVersion := "Os Maximum Version value"
androidRestriction.SetOsMaximumVersion(&osMaximumVersion) 
requestBody.SetAndroidRestriction(androidRestriction)
macOSRestriction := graphmodels.NewDeviceEnrollmentPlatformRestriction()
platformBlocked := true
macOSRestriction.SetPlatformBlocked(&platformBlocked) 
personalDeviceEnrollmentBlocked := true
macOSRestriction.SetPersonalDeviceEnrollmentBlocked(&personalDeviceEnrollmentBlocked) 
osMinimumVersion := "Os Minimum Version value"
macOSRestriction.SetOsMinimumVersion(&osMinimumVersion) 
osMaximumVersion := "Os Maximum Version value"
macOSRestriction.SetOsMaximumVersion(&osMaximumVersion) 
requestBody.SetMacOSRestriction(macOSRestriction)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
deviceEnrollmentConfigurations, err := graphClient.DeviceManagement().DeviceEnrollmentConfigurations().Post(context.Background(), requestBody, nil)


```