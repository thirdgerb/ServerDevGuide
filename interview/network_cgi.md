# CGI & Fast-cgi


## CGI

CGI : 公共网关接口（Common Gateway Interface，CGI）

本质是 Interface.

### 生命周期

Folk 新进程, 例如解释器

### 常用环境变量

- SERVER_NAME：运行CGI序为机器名或IP地址。
- SERVER_INTERFACE：WWW服务器的类型，如：CERN型或NCSA型。
- SERVER_PROTOCOL：通信协议，应当是HTTP/1.0。
- SERVER_PORT：TCP端口，一般说来web端口是80。
- HTTP_ACCEPT：HTTP定义的浏览器能够接受的数据类型。
- HTTP_REFERER：发送表单的文件URL。（并非所有的浏览器都传送这一变量）
- HTTP_USER-AGENT：发送表单的浏览的有关信息。
- GETWAY_INTERFACE：CGI程序的版本，在UNIX下为 CGI/1.1。
- PATH_TRANSLATED：PATH_INFO中包含的实际路径名。
- PATH_INFO：浏览器用GET方式发送数据时的附加路径。
- SCRIPT_NAME：CGI程序的路径名。
- QUERY_STRING：表单输入的数据，URL中问号后的内容。
- REMOTE_HOST：发送程序的主机名，不能确定该值。
- REMOTE_ADDR：发送程序的机器的IP地址。
- REMOTE_USER：发送程序的人名。
- CONTENT_TYPE：POST发送，一般为application/xwww-form-urlencoded。
- CONTENT_LENGTH：POST方法输入的数据的字节数


## Fast-cgi

使用 TCP 通信.