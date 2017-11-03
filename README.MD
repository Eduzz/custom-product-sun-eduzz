# Alterando Produto SUN Eduzz

Usando a classe no seu projeto,
primeiro crie um objeto **ProductCustomSunEduzz**:

```php
$productCustomSunEduzz = new ProductCustomSunEduzz();
```

Quando houver necessiadade, você pode alterar todo o valor do produto no Checkout Sun usando a seguinte configuração:
```php
/**
* @productValue decimal
*/
$productCustomSunEduzz->productValue = 1.99;
```

Quando você gera um Frete na sua página de vendas, é possível customizar o valor apresentado no Checkout Sun através da seguinte configuração:

```php
/**
* @zipCod String
* @deadline int
* @shippingValue decimal
*/
$productCustomSunEduzz->zipCode = '18051827';
$productCustomSunEduzz->deadline = 1;
$productCustomSunEduzz->shippingValue = 10;
```

Você tem acesso a sua PublicKey e PrivateKey no MyEduzz e seu contentId é o ID do conteúdo cadastrado no MyEduzz, depois que os dados estiverem em mãos, é só configurar:

```php
/**
* @publicKey String
* @privateKey String
* @contentId String
*/
$productCustomSunEduzz->publicKey = '123';
$productCustomSunEduzz->privateKey = '123';
$productCustomSunEduzz->contentId = '33345';
```

Caso precisar pode enviar para identificar sua transação um valor único em seu ecommerce. O orderId não é obrigatório.
```php
/**
* @orderId String
**/
$productCustomSunEduzz->orderId = 'abc';
```

Gerando apenas o Hash para enviar através do parâmetro GET na URL usando **?dataCtm=**{HASH_GERADO}
```php
echo $productCustomSunEduzz->generateBase64Hash();
```

Você também pode gerar  URL completa.
```php
echo $productCustomSunEduzz->generateUrl();
```
