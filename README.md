# Installation
Simply require the file pagination.php
```php
require 'pagination.php';
```
OR you can simply copy the function `pagination` in above file to your source code.
# Usage
```php
$baseUrl = "http://somedomain.com/users";
$totalResults = 150;
$resultsPerPage = 10;
$currentPage = !empty($_GET['page']) && ctype_digit($_GET['page']) ? $_GET['page'] : 1;
echo pagination($baseUrl, $totalResults, $resultsPerPage, $currentPage);
```

# Adding Parameters to query string
By default the paginated links will contain only the `?page=` query string. To append additional parameters to this you can pass an associative array of parameters and values as the fifth parameter
```php
$additional_params = ['name'=>'John', 'age'=>18];
echo pagination($baseUrl, $totalResults, $resultsPerPage, $currentPage, $additional_params);
```
Each paginated link will now contain `name=John&age=18&page=` as query string.

For additional explanation of this function please visit [http://perials.com/a-bootstrap-compatible-pagination-function-in-php-for-database-queries/]

[http://perials.com/a-bootstrap-compatible-pagination-function-in-php-for-database-queries/]: <http://perials.com/a-bootstrap-compatible-pagination-function-in-php-for-database-queries/>