---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new EnrollAssetsPostRequestBody();
$requestBody->setUpdateCategory(new UpdateCategory('string'));

$assets1 = new ();
$additionalData = [
'@odata.type' => '#microsoft.graph.windowsUpdates.azureADDevice', 
'id' => 'String (identifier)', 
];
$assets1->setAdditionalData($additionalData);



$assetsArray []= $assets1;
$requestBody->setAssets($assetsArray);




$graphServiceClient->admin()->windows()->updates()->updatableAssets()->enrollAssets()->post($requestBody);


```