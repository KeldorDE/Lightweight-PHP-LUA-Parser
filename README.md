Lightweight-PHP-LUA-Parser
===================

PHP Class for parsing LUA files


### Performance data: ###

| LUA File Size | PHP Memory Usage  | Execution Time |
| ------------: |------------------:| --------------:|
| 113,49 KB     | 1.25 MB           | 0.013 Sec.     |
| 1,44 MB       | 7.75 MB           | 0.149 Sec.     |
| 4,32 MB       | 11.00 MB          | 0.844 Sec.     |


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

### Example usage with optional syntax checking: ###

```php
require('parser.php');

$parser = new LUAParser();

try {

	// Add LUA keys that have to be present in the file
	// If one of the defined keys are missing an syntax error exception will be thrown
	$parser->addSyntaxKey('BookTitle');
	$parser->addSyntaxKey('CharacterName');
	$parser->addSyntaxKey('ListOfBooks');

	$parser->parseFile('data.lua');
	print_r($parser->data);
}
catch(Exception $e) {
    echo 'Exception: ',  $e->getMessage(), PHP_EOL;
}
```

### Example multiple file usage: ###

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
