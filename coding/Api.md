# Api - the Telegram Api

### What is Class- Api?
Api class is the class used to make HTTP Request on Telegram Api.
Api make it easy to use telegram Api more effectively and efficiently.

#### How we can Use It?

Its too much easy to work with Class *Api*.
You can just use it with the following syntax.

_**Syntax:**_

```php
<?php
Api::{methodName} ( array_of_data );
?>
```

Examples are given below:

```php
<?php

// Send Message With Telegram Api.

Api::sendMessage([
'chat_id' => Bot::$chat_id,
'text' => 'Hello, Demo Send Message with Api'
]);

?>
```
