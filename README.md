# Cloudinary Media Editing API PHP SDK

Cloudinary Media Editing API

For more information, please visit [https://cloudinary.com](https://cloudinary.com).

## Installation & Usage

### Requirements

PHP 7.3 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "require": {
    "cloudinary/media-editing-api": "*"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/media-editing-api/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://api.cloudinary.com/v2/demo*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*TransformApi* | [**transform**](docs/Api/TransformApi.md#transform) | **POST** /media_editing/transform | Transform a media asset
*TransformAndStoreApi* | [**transformAndStore**](docs/Api/TransformAndStoreApi.md#transformandstore) | **POST** /media_editing/transform_and_store | Transform and store media asset

## Models

- [EnqueuedResponse](docs/Model/EnqueuedResponse.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [ErrorResponseError](docs/Model/ErrorResponseError.md)
- [MediaConnectorInstance](docs/Model/MediaConnectorInstance.md)
- [TransformRequest](docs/Model/TransformRequest.md)
- [TransformResult](docs/Model/TransformResult.md)
- [TransformationDescriptor](docs/Model/TransformationDescriptor.md)

## Authorization

### basicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This Cloudinary PHP package is automatically generated.

- API version: `0.1.0-beta`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
