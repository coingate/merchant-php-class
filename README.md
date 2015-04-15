# Coingate Merchant PHP Class

### Create Order

https://developer.coingate.com/page/create-order

```
require_once('coingate_merchant.class.php');

$coingate = new CoingateMerchant(array('app_id' => 'YOUR_APP_ID', 'api_key' => 'YOUR_API_KEY', 'api_secret' => 'YOUR_API_SECRET'));

$coingate->create_order(array(
	'order_id'          => 'YOUR-CUSTOM-ORDER-ID-115',
	'price'             => 1050.99,
	'currency'          => 'USD',
	'receive_currency'  => 'EUR',
	'callback_url'      => 'https://example.com/payments/callback?token=6tCENGUYI62ojkuzDPX7Jg',
	'cancel_url'        => 'https://example.com/cart',
	'success_url'       => 'https://example.com/account/orders',
	'title'				=> 'Order #112',
	'description'       => 'Apple Iphone 6'
));

if ($coingate->success)
{
	echo 'success';
}
else
{
	echo 'fail';
}

echo $coingate->status_code;

var_dump($coingate->response);
```

### Get Order

https://developer.coingate.com/page/get-order

```
require_once('coingate_merchant.class.php');

$coingate = new CoingateMerchant(array('app_id' => 'YOUR_APP_ID', 'api_key' => 'YOUR_API_KEY', 'api_secret' => 'YOUR_API_SECRET'));

$coingate->get_order(156);

if ($coingate->success)
{
	echo 'success';
}
else
{
	echo 'fail';
}

echo $coingate->status_code;

var_dump($coingate->response);
```
