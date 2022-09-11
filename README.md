# Psr Response Mutable
## Warning
Widespread use of this decorator is not recommended! We use it to transfer it to controllers via a DI container.
## Features

- Compatible with PSR-7 (Http Message)
- Simple class
- php 7.2+

## Installation
```
composer require symbiotic/http-response-mutable 
```

## Usage
Mutable response, the decorator is made to work with the response object via a Psr container.

```php
/**
 * @var  \Psr\Http\Message\ResponseInterface $response
 **/
$response = $psr_response_instance;

$responseMutable  = new Symbiotic\Http\ResponseMutable($response);
 /**
  *  your object changes...
  **/
// Getting the original object
$response  = $responseMutable->getRealInstance();


