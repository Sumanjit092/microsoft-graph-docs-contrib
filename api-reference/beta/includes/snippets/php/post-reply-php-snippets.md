---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Groups\Item\Threads\Item\Posts\Item\Reply\ReplyPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\Post;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\ContentType;
use Microsoft\Graph\Beta\Generated\Models\Recipient;
use Microsoft\Graph\Beta\Generated\Models\EmailAddress;
use Microsoft\Graph\Beta\Generated\Models\Attachment;
use Microsoft\Graph\Beta\Generated\Models\FileAttachment;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ReplyPostRequestBody();
$post = new Post();
$postBody = new ItemBody();
$postBody->setContentType(new BodyType('text'));
$postBody->setContent('content-value');
$post->setBody($postBody);
$post->setReceivedDateTime(new \DateTime('2016-10-19T10:37:00Z'));
$post->setHasAttachments(true);
$postFrom = new Recipient();
$postFromEmailAddress = new EmailAddress();
$postFromEmailAddress->setName('name-value');
$postFromEmailAddress->setAddress('address-value');
$postFrom->setEmailAddress($postFromEmailAddress);
$post->setFrom($postFrom);
$postSender = new Recipient();
$postSenderEmailAddress = new EmailAddress();
$postSenderEmailAddress->setName('name-value');
$postSenderEmailAddress->setAddress('address-value');
$postSender->setEmailAddress($postSenderEmailAddress);
$post->setSender($postSender);
$post->setConversationThreadId('conversationThreadId-value');
$newParticipantsRecipient1 = new Recipient();
$newParticipantsRecipient1EmailAddress = new EmailAddress();
$newParticipantsRecipient1EmailAddress->setName('name-value');
$newParticipantsRecipient1EmailAddress->setAddress('address-value');
$newParticipantsRecipient1->setEmailAddress($newParticipantsRecipient1EmailAddress);
$newParticipantsArray []= $newParticipantsRecipient1;
$post->setNewParticipants($newParticipantsArray);

$post->setConversationId('conversationId-value');
$post->setCreatedDateTime(new \DateTime('2016-10-19T10:37:00Z'));
$post->setLastModifiedDateTime(new \DateTime('2016-10-19T10:37:00Z'));
$post->setChangeKey('changeKey-value');
$post->setCategories(['categories-value', ]);
$post->setId('id-value');
$postInReplyTo = new Post();
$post->setInReplyTo($postInReplyTo);
$attachmentsAttachment1 = new FileAttachment();
$attachmentsAttachment1->setOdataType('#microsoft.graph.fileAttachment');
$attachmentsAttachment1->setLastModifiedDateTime(new \DateTime('2016-10-19T10:37:00Z'));
$attachmentsAttachment1->setName('name-value');
$attachmentsAttachment1->setContentType('contentType-value');
$attachmentsAttachment1->setSize(99);
$attachmentsAttachment1->setIsInline(true);
$attachmentsAttachment1->setId('id-value');
$attachmentsArray []= $attachmentsAttachment1;
$post->setAttachments($attachmentsArray);

$requestBody->setPost($post);

$graphServiceClient->groups()->byGroupId('group-id')->threads()->byConversationThreadId('conversationThread-id')->posts()->byPostId('post-id')->reply()->post($requestBody)->wait();

```