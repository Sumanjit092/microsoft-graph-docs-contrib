---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$result = $graphServiceClient->chats()->byChatId('chat-id')->operations()->byTeamsAsyncOperationId('teamsAsyncOperation-id')->get()->wait();

```