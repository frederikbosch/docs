# exif — Reads Exif data from image

## Description

> public Intervention\Image\Image exif([string $key])

Read Exif meta data from current image. **Image object must be instantiated from file path to read the EXIF data correctly.**

**Note: PHP must be compiled in with ```--enable-exif``` to use this method. Windows users must also have the ```mbstring``` extension enabled.**

## Parameters

### key (optional)
Optionally index key to retrieve only particular data. By default all data available will be loaded.


## Return Values
Associative array of all Exif data available or mixed data for particular value. If no meta data can be found, method will return NULL.

## Examples

```php
// read all existing data into an array
$data = Image::make('public/foo.jpg')->exif();

// read model of the camera
$name = Image::make('public/foo.jpg')->exif('Model');
```

## See also

- [iptc](/api/iptc)
- [orientate](/api/orientate)
