---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Event;
use Microsoft\Graph\Generated\Models\ItemBody;
use Microsoft\Graph\Generated\Models\ContentType;
use Microsoft\Graph\Generated\Models\DateTimeTimeZone;
use Microsoft\Graph\Generated\Models\Attendee;
use Microsoft\Graph\Generated\Models\EmailAddress;
use Microsoft\Graph\Generated\Models\Type;
use Microsoft\Graph\Generated\Models\SingleValueLegacyExtendedProperty;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Event();
$requestBody->setSubject('Celebrate Thanksgiving');
$body = new ItemBody();
$body->setContentType(new BodyType('hTML'));
$body->setContent('Let\'s get together!');
$requestBody->setBody($body);
$start = new DateTimeTimeZone();
$start->setDateTime('2015-11-26T18:00:00');
$start->setTimeZone('Pacific Standard Time');
$requestBody->setStart($start);
$end = new DateTimeTimeZone();
$end->setDateTime('2015-11-26T23:00:00');
$end->setTimeZone('Pacific Standard Time');
$requestBody->setEnd($end);
$attendeesAttendee1 = new Attendee();
$attendeesAttendee1EmailAddress = new EmailAddress();
$attendeesAttendee1EmailAddress->setAddress('Terrie@contoso.com');
$attendeesAttendee1EmailAddress->setName('Terrie Barrera');
$attendeesAttendee1->setEmailAddress($attendeesAttendee1EmailAddress);
$attendeesAttendee1->setType(new AttendeeType('required'));
$attendeesArray []= $attendeesAttendee1;
$requestBody->setAttendees($attendeesArray);

$singleValueExtendedPropertiesSingleValueLegacyExtendedProperty1 = new SingleValueLegacyExtendedProperty();
$singleValueExtendedPropertiesSingleValueLegacyExtendedProperty1->setId('String {66f5a359-4659-4830-9070-00040ec6ac6e} Name Fun');
$singleValueExtendedPropertiesSingleValueLegacyExtendedProperty1->setValue('Food');
$singleValueExtendedPropertiesArray []= $singleValueExtendedPropertiesSingleValueLegacyExtendedProperty1;
$requestBody->setSingleValueExtendedProperties($singleValueExtendedPropertiesArray);


$result = $graphServiceClient->me()->events()->post($requestBody)->wait();

```