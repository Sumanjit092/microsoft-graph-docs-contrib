---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\Security\HealthIssue
use Microsoft\Graph\Beta\Generated\Models\Security\Status;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new HealthIssue();
$requestBody->setStatus(new HealthIssueStatus('closed'));

$result = $graphServiceClient->security()->identities()->healthIssues()->byHealthIssueId('healthIssue-id')->patch($requestBody)->wait();

```