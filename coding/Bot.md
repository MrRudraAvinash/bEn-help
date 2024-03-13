# Bot - the ultimate class

### What is Bot Class?
It is a class used to Call Bot Methods.
Some of the methods are listed below....

#### Bot::sendMessage(text);
It is used to send *text message* to user. Usually in Markdown Format.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| text | the text to be sent | Required |

Examples are listed:
```php
<?php
Bot::sendMessage("Hello User!");
?>
```

#### Bot::sendKeyboard(keyboard, text);

Used to send *Keyboard* to _User_ with a text. Text is in Markdown Format.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| keyboard | Keyboard Text | Required |
| text | Text to be sent | Required |

Examples are listed:

```php
<?php
$keyboard = "Balance, Info \n Profile, Exit";
Bot::sendInlineKeyboard($keyboard, "Demo Inline Keyboard In B.En");
```


#### Bot::sendInlineKeyboard(keyboard, text);

Used to send *Inline Keyboard* to _User_ with a text. Text is in Markdown Format.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| keyboard | Array of Inline Keyboard | Required |
| text | Text to be sent | Required |

Examples are listed:

```php
<?php
$inline_key = [[
array('text' => 'Demo Inline Key', 'url' => 'https://bots.engineer')
]];
Bot::sendInlineKeyboard($inline_key, "Demo Inline Keyboard In B.En");
```

#### Bot::saveData(name, value);

Used to save **Global** Property.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| name | Name of global property | Required |
| value | the value | Required |

Examples:

```php
<?php
Bot::saveData("hello", "done");
?>
```

#### Bot::getData(name);

Used to get **Global** Data.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| name | Name of global property |  Required |

Examples:

```php
<?php
$property = Bot::getData("hello");
Bot::sendMessage($property); // Inspect Your Data
?>
```

#### Bot::runCommand(command, options);

Used to run a bot command.

Parameters:

| Name | Value | Type |
| --- | --- | --- |
| command | name of command to be runned | Required |
| options | options to be passed | Optional |

Example Usage:

```php
<?php
// Command /start
Bot::runCommand("/hello");

// Command /hello
Bot::sendMessage("Hello, I am Runned");
?>
```
