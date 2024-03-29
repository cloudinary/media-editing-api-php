# Cloudinary\MediaEditing\TransformApi

All URIs are relative to https://api.cloudinary.com/v2/demo.

Method | HTTP request | Description
------------- | ------------- | -------------
[**transform()**](TransformApi.md#transform) | **POST** /media_editing/transform | Transform a media asset


## `transform()`

```php
transform($transform_request): \SplFileObject
```

Transform a media asset

Transform a media asset

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Cloudinary URL: basicAuth
$config = Cloudinary\MediaEditing\Configuration::getDefaultConfiguration()
              ->setCloudinaryUrl('cloudinary://key:secret@cloud_name');


$apiInstance = new Cloudinary\MediaEditing\Api\TransformApi(null, $config);

$transform_request = {"input_type":"url","url":"https://cloudinary-devs.github.io/cld-docs-assets/assets/images/shoes.jpg","transformation_descriptor":{"descriptor_type":"canonical","canonical_transformation":"w_500,c_scale,f_auto"}}; // \Cloudinary\MediaEditing\Model\TransformRequest

try {
    $result = $apiInstance->transform($transform_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransformApi->transform: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transform_request** | [**\Cloudinary\MediaEditing\Model\TransformRequest**](../Model/TransformRequest.md)|  | [optional]

### Return type

**\SplFileObject**

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/octet-stream`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
