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

### Multiple file usage: ###

```php
require('parser.php');

$parser = new LUAParser();

try {
	$parser->parseFile('data_file_1.lua');
	print_r($parser->data);
	
	$parser->parseFile('data_file_2.lua');
	print_r($parser->data);
	
	$parser->parseFile('data_file_3.lua');
	print_r($parser->data);
}
catch(Exception $e) {
    echo 'Exception: ',  $e->getMessage(), PHP_EOL;
}
```
