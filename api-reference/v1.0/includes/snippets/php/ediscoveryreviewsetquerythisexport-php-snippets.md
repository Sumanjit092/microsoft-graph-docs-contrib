---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Security\Cases\EdiscoveryCases\Item\ReviewSets\Item\Queries\Item\MicrosoftGraphSecurityExport\ExportPostRequestBody
use Microsoft\Graph\Generated\Models\Security\ExportOptions;
use Microsoft\Graph\Generated\Models\Security\ExportStructure;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ExportPostRequestBody();
$requestBody->setOutputName('Export reviewset query via API');
$requestBody->setDescription('Export for the Contoso investigation 2');
$requestBody->setExportOptions(new ExportOptions('originalFiles,tags'));
$requestBody->setExportStructure(new ExportFileStructure('directory'));

$graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->reviewSets()->byEdiscoveryReviewSetId('ediscoveryReviewSet-id')->queries()->byEdiscoveryReviewSetQueryId('ediscoveryReviewSetQuery-id')->microsoftGraphSecurityExport()->post($requestBody)->wait();

```