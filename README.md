# WP Strip Image Metadata (WordPress plugin)

> Strip image metadata on upload or via bulk action, and view image EXIF data.

## Description

WP Strip Image Metadata is a privacy focused WordPress plugin that helps in removing potentially sensitive metadata from your uploaded images.

## What is image metadata?

Image metadata is extra information embedded in image files. This information is stored in a variety of formats and contains items like the model of the camera that took a photo.

However, image metadata may also contain identifying information such as the GPS location coordinates of an image taken with a smartphone for example.

This plugin provides an easy enabled/disabled setting so you can make the call on when image metadata should be removed.

**Note**: this plugin requires the "Imagick" or "Gmagick" PHP extension to function.

## Frequently Asked Questions

### How will I know if I have the required Imagick or Gmagick extension on my site?

If you aren't sure, after installing the plugin, in WP Admin navigate to: Settings > Strip Image Metadata

Under "Plugin Information" it will show if the required extension is active on the site or not.

If a compatible extension is not found, try asking your webhost or system administrator if either one can be enabled.

### Can I remove metadata from images uploaded before installing this plugin?

Yes, there is a bulk action included. In WP Admin navigate to the Media library and make sure you are using the List view.

Select which images you'd like to strip metadata from and then select the "WP Strip Image Metadata" bulk action.

This can be a resource intensive process, so please only select a handful of images at one time for processing.

### Will this work for all generated image subsizes (thumbnails)?

Yes, if metadata stripping is enabled then all generated subsizes at the time of upload will have the metadate removed.

The included bulk action will also remove metadata from all subsizes as well.

### How do I know it's working?

In WP Admin, from your Media library you can select an image and click "Edit" (in List view) or "Edit more details" (in Grid view).

On the Edit page for the image, there will be an admin notice at the top with the "expand for image EXIF data" text. This should work for jpg/jpeg files, but other image types may not display EXIF info.

You might try uploading a test image with the "Image Metadata Stripping" setting disabled, and then the same image again with the setting enabled to view the difference.

Here are some good sample images for testing: https://github.com/ianare/exif-samples/tree/master/jpg/gps

Popular image editing applications such as Photoshop or Affinity Photo also have the capability to inspect image metadata which can prove useful.

### Once image metadata has been stripped, is it reversible?

No, removing image metadata is permanent. If you would like the metadata kept, you should keep an offsite backup copy of your images.

### What file types does this plugin work for?

By default the plugin will process jpg/jpeg files.

To add other file types you can use the `wp_strip_image_metadata_image_file_types` filter.

### What do the plugin settings do?

* Image Metadata Stripping: whether image metadata is stripped from new uploads.
* Preserve ICC Color Profile: whether to keep image color information which is helpful to some applications.
* Preserve Image Orientation: whether to keep image orientation which can help rotate images as intended.
* Log Errors: whether to log error output which can be helpful for debugging purposes.

## Changelog

### 1.0 - 2022-06-12

- Initial plugin release.

[See the previous changelogs here](https://github.com/samiff/wp-strip-image-metadata/blob/main/CHANGELOG.md)
