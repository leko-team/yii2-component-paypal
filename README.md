# leko-team/yii2-component-paypal

## Description

The PayPal payment system component for the Yii2 framework.

## Installation

* Install curl:

```terminal
$ sudo apt-get install libcurl3 php5-curl
```

* Add to your composer.json file at the project:

```json
"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/leko-team/yii2-component-paypal.git"
    }
],
"require": {
    "leko-team/yii2-component-paypal": "dev-master"
},
```

* Run composer update at the project:

```terminal
$ composer update
```

## Settings

> This is sapmle settings for yii2-app-advanced project.

* Add to your "main.php" config file this part with component params:

```php        
'components' => [
    'lekoPayPal' => [
        'class'  => 'leko\components\paypal\PayPal',
        'config' => [
            'returnUrl' => '/controller/action',
            'cancelUrl' => '/controller/action',
            'version'   => XXX.X,    // PayPal API version (e.g. 124.0)
        ],
    ],
],
```

* Add to your "main-local.php" config file this part with required params:

```php        
'components' => [
    'lekoPayPal' => [
        'config' => [
            'user'      => 'your_user_id',
            'password'  => 'your_password',
            'signature' => 'your_signature', 
            'mode'      => 'payment_mode',   // 'sandbox' or 'live'
        ],
    ],
],
```

> In "config" section you may add some non-required params:
* url - payment system url for curl request (def. "api-3t.sandbox.paypal.com/nvp");
* checkoutUrl - payment system redirect url for pay on PayPal site from client account or created account (def. "www.sandbox.paypal.com/cgi-bin/webscr?cmd=_express-checkout&token=");
* timeout - timeout for curl request to payment system (sec) (def. 0);

## Usage
> TODO
