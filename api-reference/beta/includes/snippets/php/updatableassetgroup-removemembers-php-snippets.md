---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Admin\Windows\Updates\UpdatableAssets\Item\MicrosoftGraphWindowsUpdatesRemoveMembers\RemoveMembersPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\UpdatableAsset
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\AzureADDevice


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new RemoveMembersPostRequestBody();
$assetsUpdatableAsset1 = new AzureADDevice();
$assetsUpdatableAsset1->setOdataType('#microsoft.graph.windowsUpdates.azureADDevice');
$assetsUpdatableAsset1->setId('String (identifier)');
$assetsArray []= $assetsUpdatableAsset1;
$requestBody->setAssets($assetsArray);


$graphServiceClient->admin()->windows()->updates()->updatableAssets()->byUpdatableAssetId('updatableAsset-id')->microsoftGraphWindowsUpdatesRemoveMembers()->post($requestBody)->wait();

```