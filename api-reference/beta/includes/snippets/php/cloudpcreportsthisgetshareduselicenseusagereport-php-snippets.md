---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\DeviceManagement\VirtualEndpoint\Reports\GetSharedUseLicenseUsageReport\GetSharedUseLicenseUsageReportPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\ReportName;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new GetSharedUseLicenseUsageReportPostRequestBody();
$requestBody->setReportName(new CloudPcReportName('sharedUseLicenseUsageReport'));
$requestBody->setFilter('ServicePlanId eq \'2d1d344e-d10c-41bb-953b-b3a47521dca0\' and DateTimeUTC gt datetime\'2022-11-30\'');
$requestBody->setSelect(['ServicePlanId', 'LicenseCount', 'ClaimedLicenseCount', 'DateTimeUTC', 	]);
$requestBody->setSkip(0);
$requestBody->setTop(100);

$graphServiceClient->deviceManagement()->virtualEndpoint()->reports()->getSharedUseLicenseUsageReport()->post($requestBody)->wait();

```