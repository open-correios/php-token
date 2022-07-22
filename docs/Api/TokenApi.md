# OpenCorreios\TokenApi

All URIs are relative to https://api.correios.com.br/token.

| Method                                             | HTTP request                          | Description                                        |
|----------------------------------------------------|---------------------------------------|----------------------------------------------------|
| [**tokenPorCartao()**](TokenApi.md#tokenPorCartao) | **POST** /v1/autentica/cartaopostagem | Gera um token para usuários externos (idCorreios). |

## `tokenPorCartao()`

```php
tokenPorCartao($cartaoPostagemRequest): \OpenCorreios\Model\Token
```

Gera um token para usuários externos (idCorreios).

Para acessar APIs cuja autorização seja por cartão de postagem.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenCorreios\Api\TokenApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cartaoPostagemRequest = new \OpenCorreios\Model\CartaoPostagemRequest(); // \OpenCorreios\Model\CartaoPostagemRequest

try {
    $result = $apiInstance->tokenPorCartao($cartaoPostagemRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenApi->tokenPorCartao: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name                      | Type                                                                               | Description | Notes      |
|---------------------------|------------------------------------------------------------------------------------|-------------|------------|
| **cartaoPostagemRequest** | [**\OpenCorreios\Model\CartaoPostagemRequest**](../Model/CartaoPostagemRequest.md) |             | [optional] |

### Return type

[**\OpenCorreios\Model\Token**](../Model/Token.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
