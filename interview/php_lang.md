# PHP 语法要点

## include & require

include与require除了在处理引入文件的方式不同外，最大的区别就是：include在引入不存文件时产生一个警告且脚本还会继续执行，而require则会导致一个致命性错误且脚本停止执行。

include()与require()的功能相同，但在用法上却有一些不同，include()是有条件包含函数，而 require()则是无条件包含函数。


- [1] [PHP函数include include_once require和require_once的区别](https://www.cnblogs.com/phpfensi/p/7861127.html)