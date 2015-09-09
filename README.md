# Coingate Merchant PHP Class

### Create Order

https://developer.coingate.com/docs/create-order

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

echo 'Response HTTP Status: ' . $coingate->status_code . "\n";

if ($coingate->success)
{
	echo 'SUCCESS' . "\n";
	var_dump(json_decode($coingate_service->response));
}
else
{
	echo 'FAIL' . "\n";
	echo $coingate_service->response;
}
```

### Get Order

https://developer.coingate.com/docs/get-order

```
require_once('coingate_merchant.class.php');

$coingate_service = new CoingateMerchant(array('app_id' => '6', 'api_key' => 'zLn5q7GuOxNXWoyQ2HpUiY', 'api_secret' => 'Uv7huPCYVcmAR4oX5zIwOSHFT8gbDBpZ'));

$coingate_service->get_order(1087999);

echo 'Response HTTP Status: ' . $coingate_service->status_code . "\n";

if ($coingate_service->success)
{
	echo 'SUCCESS' . "\n";
	var_dump(json_decode($coingate_service->response));
}
else
{
	echo 'FAIL' . "\n";
	echo $coingate_service->response;
}
```
