---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Security\Cases\EdiscoveryCases\Item\Custodians\MicrosoftGraphSecurityUpdateIndex\UpdateIndexPostRequestBody


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UpdateIndexPostRequestBody();
$requestBody->setIds(['7f697316-43ed-48e1-977f-261be050db93', 'b26888b3-e1f5-47c5-bdf2-33d1b90cb2e8', 	]);

$graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->custodians()->microsoftGraphSecurityUpdateIndex()->post($requestBody)->wait();

```