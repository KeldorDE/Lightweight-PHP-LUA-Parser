Lightweight-PHP-LUA-Parser
===================

PHP Class for parsing LUA files

### Example usage: ###

```php
// Include the parser class
require('parser.php');

// Initialise the paraser
$parser = new LUAParser();

// Catch parser exceptions
try {

	// Parse a LUA file
	$parser->parseFile('data.lua');

	// Print the parsed array
	print_r($parser->data);
}
catch(Exception $e) {
    echo 'Exception: ',  $e->getMessage(), PHP_EOL;
}
```
