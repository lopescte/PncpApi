API do PNCP - Portal Nacional de Compras Públicas
======

[![Latest Stable Version](http://poser.pugx.org/lopescte/pncpapi/v)](https://packagist.org/packages/lopescte/PncpApi)
[![Total Downloads](http://poser.pugx.org/lopescte/pncpapi/downloads)](https://packagist.org/packages/lopescte/PncpApi)
[![PHP Version Require](http://poser.pugx.org/lopescte/pncpapi/require/php)](https://packagist.org/packages/lopescte/PncpApi)
[![License](http://poser.pugx.org/lopescte/pncpapi/license)](https://packagist.org/packages/lopescte/PncpApi)

API para conexão e envio de dados para o Portal Nacional de Contratações Públicas - PNCP - do Governo Federal Brasileiro, criado pela Lei de Licitações e Contratos Administrativos (Lei nº 14.133/2021).

## Easy Installation

### Install with composer

To install with [Composer](https://getcomposer.org/), simply require the
latest version of this package.

```bash
composer require lopescte/pncp-api
```

Make sure that the autoload file from Composer is loaded.

```php
// somewhere early in your project's loading, require the Composer autoloader
// see: http://getcomposer.org/doc/00-intro.md
require 'vendor/autoload.php';

```

## Usage

Easy to use in your php files or classes, as below:

```php
use Lopescte\Pncp;

$breadcrumb = new TBreadCrumbWithLink;
$breadcrumb->addItem('You are here:',NULL,TRUE);
$breadcrumb->addItem('Home', 'MyHomeClassName',FALSE);
$breadcrumb->renderFromXML('MyMenu.xml', __CLASS__);
```

## Author

* **Marcelo Lopes** - *Developer* - [Site](https://www.reiselopes.com.br) | [Facebook](https://facebook.com/lopes.cte) | [Instagram](https://instagram.com/lopescte) | [Twitter](https://twitter.com/lopescte/) | [GitHub](https://github.com/lopescte)


## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.