---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\IndustryData\AdministrativeUnitProvisioningFlow
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\IndustryData\AdminUnitCreationOptions


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AdministrativeUnitProvisioningFlow();
$requestBody->setOdataType('#microsoft.graph.industryData.administrativeUnitProvisioningFlow');
$creationOptions = new AdminUnitCreationOptions();
$creationOptions->setCreateBasedOnOrg(true);
$creationOptions->setCreateBasedOnOrgPlusroleGroup(true);
$requestBody->setCreationOptions($creationOptions);

$result = $graphServiceClient->external()->industryData()->outboundProvisioningFlowSets()->byOutboundProvisioningFlowSetId('outboundProvisioningFlowSet-id')->provisioningFlows()->post($requestBody)->wait();

```