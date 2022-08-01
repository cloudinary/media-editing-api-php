# Cloudinary\MediaEditing\TransformAndStoreApi

All URIs are relative to https://api.cloudinary.com/v2/demo.

Method | HTTP request | Description
------------- | ------------- | -------------
[**transformAndStore()**](TransformAndStoreApi.md#transformAndStore) | **POST** /media_editing/transform_and_store | Transform and store media asset


## `transformAndStore()`

```php
transformAndStore($transform_request): \Cloudinary\MediaEditing\Model\TransformResult
```

Transform and store media asset

Transform and store media asset

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Cloudinary URL: basicAuth
$config = Cloudinary\MediaEditing\Configuration::getDefaultConfiguration()
              ->setCloudinaryUrl('cloudinary://key:secret@cloud_name');


$apiInstance = new Cloudinary\MediaEditing\Api\TransformAndStoreApi(null, $config);

$transform_request = {"input_type":"url","url":"https://cloudinary-devs.github.io/cld-docs-assets/assets/images/shoes.jpg","transformation_descriptor":{"descriptor_type":"canonical","canonical_transformation":"w_500,c_scale,f_auto"}}; // \Cloudinary\MediaEditing\Model\TransformRequest

try {
    $result = $apiInstance->transformAndStore($transform_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransformAndStoreApi->transformAndStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transform_request** | [**\Cloudinary\MediaEditing\Model\TransformRequest**](../Model/TransformRequest.md)|  | [optional]

### Return type

[**\Cloudinary\MediaEditing\Model\TransformResult**](../Model/TransformResult.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
