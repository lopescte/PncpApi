API do PNCP - Portal Nacional de Compras Públicas
======

[![Latest Stable Version](http://poser.pugx.org/lopescte/pncp-api/v)](https://packagist.org/packages/lopescte/pncp-api)
[![Total Downloads](http://poser.pugx.org/lopescte/pncp-api/downloads)](https://packagist.org/packages/lopescte/pncp-api)
[![PHP Version Require](http://poser.pugx.org/lopescte/pncp-api/require/php)](https://packagist.org/packages/lopescte/pncp-api)
[![License](http://poser.pugx.org/lopescte/pncp-api/license)](https://packagist.org/packages/lopescte/pncp-api)

API para conexão e envio de dados para o Portal Nacional de Contratações Públicas - PNCP - do Governo Federal Brasileiro, criado pela Lei de Licitações e Contratos Administrativos (Lei nº 14.133/2021).

## Instalação

### Instale com o composer

Para instalar com o [Composer](https://getcomposer.org/), simplesmente faça um require para a
última versão deste pacote.

```bash
composer require lopescte/pncp-api
```

Certifique-se que o arquivo autoload do composer está carregado.

```php
// somewhere early in your project's loading, require the Composer autoloader
// see: http://getcomposer.org/doc/00-intro.md
require 'vendor/autoload.php';

```

## Uso

Primeiro inicialize a conexão ao PNCP com suas credenciais, como abaixo:

```php
use Lopescte\PncpApi\Pncp;

$pncp = new Pncp($seu_login_pncp, $sua_senha_pncp, $ambiente_pncp); // $ambiente_pncp por padrão é setado para 1 (Homologação); Para ambiente de produção, sete 2 nesta variável.
```

Com a conexão inicializada, utilize qualquer das classes de funções chamando-as diretamente, sem se esquecer de declarar o uso, como abaixo:

```php
use Lopescte\PncpApi\Usuarios;

$usuario = new Usuarios;

$usuario->buscaUsuarioPorId($seu_id_de_usuario_do_pncp);

if($usuario->response['entesAutorizados'])
{
    foreach($usuario->response['entesAutorizados'] as $entidade)
    {
        // Verifique aqui se o órgão que vc necessita está nas suas entidades autorizadas
    }  
}

// Para inserir autorização para algum órgão faça assim:

$usuario->insereEntesUsuarioPorId((int) $seu_id_de_usuario_do_pncp, $cnpj_do_orgao);
```

As respostas da API após uma chamada de função serão sempre um objeto como abaixo:

```php
if($usuario->response)
{
    // Sua lógica aqui  
}
```

## Author

* **Marcelo Lopes** - *Developer* - [Site](https://www.reiselopes.com.br) | [Facebook](https://facebook.com/lopes.cte) | [Instagram](https://instagram.com/lopescte) | [Twitter](https://twitter.com/lopescte/) | [GitHub](https://github.com/lopescte)


## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.