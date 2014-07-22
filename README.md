Nearest UK Postcode Finder
==========================

This library takes a UK postcode outcode (the bit before the space) and a radius, and returns all other uk postcodes within that radius.

It is powered by a csv file of postcodes and their longitude and latitude coordinates, and should not be used in production environments where speed is important.

Usage
-----
Create a postcode:
```php
$postcode = new Jflight\PostcodeFinder\UkPostcode('CF11');
```
Return an array of nearby postcodes:
```php
$nearbyPostcodes = $postcode->findNearestPostcodes(10)); // Distance in km
```

Extension
---------
In theory, the library could be used for postcodes (or equivalent) for any county, as long as csv lookup of postcodes with their longitude and latitue is available.

This would be done as follows:

```php
<?php

namespace Jflight\PostcodeFinder;

class NewPostcode extends Postcode {
    protected $file = "/path/to/csv.csv";
}
```