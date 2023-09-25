---
title: PHP Type Juggling
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---


# Type Juggling

> Type Juggling vulnerable versions of PHP 
> 
> \> 8.0.0
{: .block-warning }

~~~ php
// 7.4.33 version
<?php
    echo var_dump( "0abc" == (int)"0000000000" );
?>

// Result : bool(true)
~~~

~~~ php
// 8.3.0 version
<?php
    echo var_dump( "0abc" == (int)"0000000000" );
?>

// Result : bool(false)
~~~

<br>


~~~ php
<?php
    echo sha1("1");
?>

// Result : 356a192b7913b04c54574d18c28d46e6395428ab
~~~


~~~ php
// 7.4.33 version
<?php
    echo var_dump( (int)"356abcde" == sha1("1") );
?>

// Result : bool(true)
~~~



# Loose(==) comparisons Table
![/assets/gitbook/images/2023-09-25/php-loose-comparisons.PNG](/assets/gitbook/images/2023-09-25/php-loose-comparisons.PNG)

# Strict(===) comparisons Table
![/assets/gitbook/images/2023-09-25/php-strict-comparisons.PNG](/assets/gitbook/images/2023-09-25/php-strict-comparisons.PNG)





