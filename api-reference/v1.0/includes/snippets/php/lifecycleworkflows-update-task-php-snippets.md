---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\Task


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Task();
$requestBody->setDescription('Add user to selected groups');
$requestBody->setDisplayName('Update marketing day 1 add users to Group set up');

$result = $graphServiceClient->identityGovernance()->lifecycleWorkflows()->workflows()->byWorkflowId('workflow-id')->tasks()->byTaskId('task-id')->patch($requestBody)->wait();

```