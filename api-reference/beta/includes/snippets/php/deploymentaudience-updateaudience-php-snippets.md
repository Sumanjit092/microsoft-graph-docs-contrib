---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Admin\Windows\Updates\DeploymentAudiences\Item\MicrosoftGraphWindowsUpdatesUpdateAudience\UpdateAudiencePostRequestBody
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\UpdatableAsset
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\AzureADDevice


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UpdateAudiencePostRequestBody();
$addMembersUpdatableAsset1 = new AzureADDevice();
$addMembersUpdatableAsset1->setOdataType('#microsoft.graph.windowsUpdates.azureADDevice');
$addMembersUpdatableAsset1->setId('String (identifier)');
$addMembersArray []= $addMembersUpdatableAsset1;
$requestBody->setAddMembers($addMembersArray);


$graphServiceClient->admin()->windows()->updates()->deploymentAudiences()->byDeploymentAudienceId('deploymentAudience-id')->microsoftGraphWindowsUpdatesUpdateAudience()->post($requestBody)->wait();

```