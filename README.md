DigitalOcean V2
===============

Let's consume the [DigitalOcean API V2](https://github.com/digitaloceancloud/api-v2-docs) :)
This libray is in *work in progress* as well as the *API*.

[![Build Status](https://secure.travis-ci.org/toin0u/DigitalOceanV2.png)](http://travis-ci.org/toin0u/DigitalOceanV2)
[![Latest Stable Version](https://poser.pugx.org/toin0u/digitalocean-v2/v/stable.svg)](https://packagist.org/packages/toin0u/digitalocean-v2)
[![Total Downloads](https://poser.pugx.org/toin0u/digitalocean-v2/downloads.png)](https://packagist.org/packages/toin0u/digitalocean-v2)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/5b4eac7e-c83b-4913-86e1-72950821757a/mini.png)](https://insight.sensiolabs.com/projects/5b4eac7e-c83b-4913-86e1-72950821757a)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/toin0u/DigitalOceanV2/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/toin0u/DigitalOceanV2/?branch=master)

TODO
----

- [x] [Actions](https://developers.digitalocean.com/v2/#actions)
- [x] [Domain records](https://developers.digitalocean.com/v2/#domain-records)
- [x] [Domains](https://developers.digitalocean.com/v2/#domains)
- [ ] [Droplet actions](https://developers.digitalocean.com/v2/#droplet-actions)
- [ ] [Droplets](https://developers.digitalocean.com/v2/#droplets)
- [x] [Image actions](https://developers.digitalocean.com/v2/#image-actions)
- [x] [Images](https://developers.digitalocean.com/v2/#images)
- [ ] [Keys](https://developers.digitalocean.com/v2/#keys)
- [x] [Regions](https://developers.digitalocean.com/v2/#regions)
- [x] [Sizes](https://developers.digitalocean.com/v2/#sizes)

Installation
------------

This library can be found on [Packagist](https://packagist.org/packages/toin0u/digitalocean-v2).
The recommended way to install this is through [composer](http://getcomposer.org).

Run these commands to install composer, the library and its dependencies:

```bash
$ curl -sS https://getcomposer.org/installer | php
$ php composer.phar require toin0u/digitalocean-v2:@dev
```

Or edit `composer.json` and add:

```json
{
    "require": {
        "toin0u/digitalocean-v2": "@dev"
    }
}
```

Example
-------

```php
<?php

require 'vendor/autoload.php';

use DigitalOceanV2\Adapter\BuzzAdapter;
use DigitalOceanV2\DigitalOceanV2;

$adapter = new BuzzAdapter('your_access_token');
$digitalOcean = new DigitalOceanV2($adapter);

$action = $digitalOcean->action();

try {
    var_dump($action->getAll());
    var_dump($action->getById(12345));
} catch (Exception $e) {
    die($e->getMessage());
}
```

Contributing
------------

Please see [CONTRIBUTING](https://github.com/toin0u/DigitalOceanV2/blob/master/CONTRIBUTING.md) for details.

Credits
-------

* [Antoine Corcy](https://twitter.com/toin0u)
* [Yassir Hannoun](https://twitter.com/yassirh)
* [All contributors](https://github.com/toin0u/DigitalOceanV2/contributors)

Support
-------

[Please open an issues in github](https://github.com/toin0u/DigitalOceanV2/issues)

License
-------

DigitalOceanV2 is released under the MIT License. See the bundled
[LICENSE](https://github.com/toin0u/DigitalOceanV2/blob/master/LICENSE) file for details.
