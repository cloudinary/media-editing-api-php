# # TransformRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_type** | **string** | The media input type |
**resource_type** | **string** | The resource type to be processed | [optional]
**url** | **string** | URL of the asset to be transformed | [optional]
**media_source** | [**\Cloudinary\Model\MediaConnectorInstance**](MediaConnectorInstance.md) |  | [optional]
**transformation_descriptor** | [**\Cloudinary\Model\TransformationDescriptor**](TransformationDescriptor.md) |  |
**async** | **bool** | Whether to perform the request asynchronously. Use a notification URL to be notified once the transformation has completed | [optional]
**notification_url** | **string** | The URL to send notifications once a transformation has completed | [optional]
**media_target** | [**\Cloudinary\Model\MediaConnectorInstance**](MediaConnectorInstance.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
