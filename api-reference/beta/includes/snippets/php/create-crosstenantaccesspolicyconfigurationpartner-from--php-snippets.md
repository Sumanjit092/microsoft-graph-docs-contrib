---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyConfigurationPartner;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyB2BSetting;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTargetConfiguration;
use Microsoft\Graph\Beta\Generated\Models\AccessType;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTarget;
use Microsoft\Graph\Beta\Generated\Models\TargetType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CrossTenantAccessPolicyConfigurationPartner();
$requestBody->setTenantId('3d0f5dec-5d3d-455c-8016-e2af1ae4d31a');
$b2bDirectConnectOutbound = new CrossTenantAccessPolicyB2BSetting();
$b2bDirectConnectOutboundUsersAndGroups = new CrossTenantAccessPolicyTargetConfiguration();
$b2bDirectConnectOutboundUsersAndGroups->setAccessType(new CrossTenantAccessPolicyTargetConfigurationAccessType('blocked'));
$targetsCrossTenantAccessPolicyTarget1 = new CrossTenantAccessPolicyTarget();
$targetsCrossTenantAccessPolicyTarget1->setTarget('6f546279-4da5-4b53-a095-09ea0cef9971');
$targetsCrossTenantAccessPolicyTarget1->setTargetType(new CrossTenantAccessPolicyTargetType('group'));
$targetsArray []= $targetsCrossTenantAccessPolicyTarget1;
$b2bDirectConnectOutboundUsersAndGroups->setTargets($targetsArray);

$b2bDirectConnectOutbound->setUsersAndGroups($b2bDirectConnectOutboundUsersAndGroups);
$requestBody->setB2bDirectConnectOutbound($b2bDirectConnectOutbound);
$b2bDirectConnectInbound = new CrossTenantAccessPolicyB2BSetting();
$b2bDirectConnectInboundApplications = new CrossTenantAccessPolicyTargetConfiguration();
$b2bDirectConnectInboundApplications->setAccessType(new CrossTenantAccessPolicyTargetConfigurationAccessType('allowed'));
$targetsCrossTenantAccessPolicyTarget1 = new CrossTenantAccessPolicyTarget();
$targetsCrossTenantAccessPolicyTarget1->setTarget('Office365');
$targetsCrossTenantAccessPolicyTarget1->setTargetType(new CrossTenantAccessPolicyTargetType('application'));
$targetsArray []= $targetsCrossTenantAccessPolicyTarget1;
$b2bDirectConnectInboundApplications->setTargets($targetsArray);

$b2bDirectConnectInbound->setApplications($b2bDirectConnectInboundApplications);
$requestBody->setB2bDirectConnectInbound($b2bDirectConnectInbound);

$result = $graphServiceClient->policies()->crossTenantAccessPolicy()->partners()->post($requestBody)->wait();

```