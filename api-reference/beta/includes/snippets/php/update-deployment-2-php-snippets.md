---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\Deployment
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\DeploymentSettings
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\MonitoringSettings
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\WindowsUpdates\MonitoringRule
use Microsoft\Graph\Beta\Generated\Models\WindowsUpdates\Signal;
use Microsoft\Graph\Beta\Generated\Models\WindowsUpdates\Action;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Deployment();
$requestBody->setOdataType('#microsoft.graph.windowsUpdates.deployment');
$settings = new DeploymentSettings();
$settings->setOdataType('microsoft.graph.windowsUpdates.deploymentSettings');
$settingsMonitoring = new MonitoringSettings();
$monitoringRulesMonitoringRule1 = new MonitoringRule();
$monitoringRulesMonitoringRule1->setSignal(new MonitoringSignal('rollback'));
$monitoringRulesMonitoringRule1->setThreshold(5);
$monitoringRulesMonitoringRule1->setAction(new MonitoringAction('pauseDeployment'));
$monitoringRulesArray []= $monitoringRulesMonitoringRule1;
$settingsMonitoring->setMonitoringRules($monitoringRulesArray);

$settings->setMonitoring($settingsMonitoring);
$requestBody->setSettings($settings);

$result = $graphServiceClient->admin()->windows()->updates()->deployments()->byDeploymentId('deployment-id')->patch($requestBody)->wait();

```