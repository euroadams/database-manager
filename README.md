# Database Manager
An SQL injection proofed PHP class for managing data base query routines using PDO



> [!CAUTION]
> All example codes herein are strictly for illustration purposes only. It's recommended to optimize before using for production.

## Instantiating the Class :

The `DataBaseManager` can be instantiated using the standard PHP syntax as follows

```php

<?php

$DBM = new DataBaseManager($dsn, $dbUser, $dbPwd, $options = array());


/****
 *  @param $dsn => data source name E.g "mysql:host=".DB_HOST.";dbname=".DB_NAME
 * 
 *  @param $dbUser => The database username
 * 
 *  @param $dbPwd => The database user password
 * 
 *  @param $options => Other optional configuration options for the database connection
 *  
 ****/        


?>

```

## Features & Usage Guide :


### Basic Safe Query Execution :
To execute SQL Injection proofed query, simply call the `doSecuredQuery()` method as shown below 

```php

<?php

$sql = "SELECT ID, FIELD_1, FIELD_2, FIELD_3  FROM my_table WHERE (FIELD_1 = ? AND FIELD_3 = ?) ORDER BY FIELD_NAME DESC LIMIT 50";

$valArr = array($value_1, $value_2);

$stmt = $DBM->doSecuredQuery($sql, $valArr);

while($row = $DBM->fetchRow($stmt)){

    // Accumulate records

}

/****
 * 
 *  @param $sql => The query string to be executed
 *  @param $valArr => An array of values for the placeholders used in the query string
 * 
 ****/        

?>

```


###  MORE DOCUMENTATION LOADING SOON :

