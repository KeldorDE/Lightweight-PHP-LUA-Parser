Lightweight-PHP-LUA-Parser
===================

PHP Class for parsing LUA files

### Example usage: ###

```php
require('parser.php');

$parser = new LUAParser();

try {
	$parser->parseFile('data.lua');
	print_r($parser->data);
}
catch(Exception $e) {
    echo 'Exception: ',  $e->getMessage(), PHP_EOL;
}
```
