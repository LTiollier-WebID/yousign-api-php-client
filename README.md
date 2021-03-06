# yousign-api-php-client

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Build Status][ico-travis]][link-travis]
[![Coverage Status][ico-scrutinizer]][link-scrutinizer]
[![Quality Score][ico-code-quality]][link-code-quality]
[![Total Downloads][ico-downloads]][link-downloads]

Yousign REST API Client.

## Structure

```
src/
tests/
examples/
```

## Install

Via Composer

``` bash
$ composer require timothecrespy/yousign-api-php-client
```

## Usage

### Framework agnostic
``` php
use TimotheCrespy\YousignClient;

// It is recommended to store this value in a .env or equivalent file (and the API key, too)
const YOUSIGN_PRODUCTION_API_URL = 'https://api.yousign.com';

$yousignClient = new YousignClient([
    'api_url' => self::YOUSIGN_PRODUCTION_API_URL,
    'api_key' => '[YOUR_PRODUCTION_API_KEY]'
]);
```

As the Yousign production API is not free, you might want to test it, with the staging environment:

``` php
use TimotheCrespy\YousignClient;

// It is recommended to store this value in a .env or equivalent file (like the API key)
const YOUSIGN_STAGING_API_URL = 'https://staging-api.yousign.com';

$yousignClient = new YousignClient([
    'api_url' => self::YOUSIGN_STAGING_API_URL,
    'api_key' => '[YOUR_STAGING_API_KEY]'
]);
```

### Laravel

```php
// If you are using Laravel (https://github.com/laravel/laravel), you could specify the default Laravel logger:
$loggerInstance = Illuminate\Support\Facades\Log::getLogger();
$yousignClient->setLogger($loggerInstance);

$yousignClient->getUsers();
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CODE_OF_CONDUCT](CODE_OF_CONDUCT.md) for details.

## Security

If you discover any security related issues, please email contact@timothecrespy.fr instead of using the issue tracker.

## Credits

- [Timothé Crespy][link-author]
- [All Contributors][link-contributors]

### Special thanks

- [Julien Cauvin](https://github.com/jucau)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/timothecrespy/yousign-api-php-client.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/timothecrespy/yousign-api-php-client/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/timothecrespy/yousign-api-php-client.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/timothecrespy/yousign-api-php-client.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/timothecrespy/yousign-api-php-client.svg?style=flat-square
[link-packagist]: https://packagist.org/packages/timothecrespy/yousign-api-php-client
[link-travis]: https://travis-ci.org/timothecrespy/yousign-api-php-client
[link-scrutinizer]: https://scrutinizer-ci.com/g/timothecrespy/yousign-api-php-client/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/timothecrespy/yousign-api-php-client
[link-downloads]: https://packagist.org/packages/timothecrespy/yousign-api-php-client

[link-author]: hhttps://github.com/TimotheCrespy
[link-contributors]: https://github.com/TimotheCrespy/yousign-api-php-client/graphs/contributors