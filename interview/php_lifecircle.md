# PHP 生命周期

## php 架构

- Application
    - SAPI
        - PHP API
        - Extension
        - PHP
    - Zend
        - Zend API
        - Zend Extension
        - Zend Engine

## SAPI

- SAPI (Server Application Programming Interface)
    - web 模式
    - CLI 模式
    - FPM
- 关键周期
    - MINT (module init)
    - RINT (request init)
    - 逻辑 (php_execute_script)
    - RSHUTDOWN(request shutdown)
    - MSHUTDOWN(module shutdown)
- 编译过程
    - zend_compile_file => OPCode
    - zend_execute

## 字节码

解释器 (脚本 => 中间码 or 操作码)

## 用户关键函数

- autoload_register
- register_shutdown
- fastcgi_finish_request

## 垃圾回收 (GC)

## JIT

## 相关文章

* [1] [PHP的工作原理和生命周期](https://www.cnblogs.com/applelife/p/10511837.html)
* [2] [PHP解释器引擎执行流程](https://www.cnblogs.com/LittleHann/p/5165928.html)