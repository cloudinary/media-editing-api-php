# Cloudinary\TransformApi

All URIs are relative to https://api.cloudinary.com/v2.

Method | HTTP request | Description
------------- | ------------- | -------------
[**transform()**](TransformApi.md#transform) | **POST** /{cloud_name}/media_editing/transform | Transform a media asset


## `transform()`

```php
transform($cloud_name, $transform_request): \Cloudinary\Model\TransformResult
```

Transform a media asset

Transform a media asset

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = Cloudinary\Configuration::getDefaultConfiguration()
              ->setCloudinaryUrl('cloudinary://key:secret@cloud_name');


$apiInstance = new Cloudinary\Api\TransformApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cloud_name = my_cloud; // string | Name of the Cloud
$transform_request = {"input_type":"url","url":"https://res.cloudinary.com/demo/image/upload/demo.jpg","transformation_descriptor":{"descriptor_type":"canonical","canonical_transformation":"w_500,c_scale,f_auto"}}; // \Cloudinary\Model\TransformRequest

try {
    $result = $apiInstance->transform($cloud_name, $transform_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransformApi->transform: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cloud_name** | **string**| Name of the Cloud |
 **transform_request** | [**\Cloudinary\Model\TransformRequest**](../Model/TransformRequest.md)|  | [optional]

### Return type

[**\Cloudinary\Model\TransformResult**](../Model/TransformResult.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/octet-stream`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
