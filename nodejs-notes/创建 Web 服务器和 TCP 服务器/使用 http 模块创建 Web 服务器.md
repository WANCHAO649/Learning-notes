* Web服务器基本知识
* 使用核心模块http创建Web服务器

Web服务器的功能：
* 接受HTTP请求（GET、POST、DELETE、PUT、PATCH）
* 处理HTTP请求（自己处理，或请求别的程序处理）
* 做出响应（返回页面、文件、各类数据等）

常见的Web服务器架构：
* Nginx/Apache：负责接受HTTP请求，并返回请求的结果
* php-fpm/php模块：处理分配给自己的请求，并将处理结果返回给分配者

常见请求种类：
* 请求文件：包括静态文件（网页、图片、前端JavaScript文件、css文件......），及由程序处理得到的文件
* 完成特定的操作：如登陆、获取特定数据等

Node.js的Web服务器：
* 不依赖其他特定的Web服务器软件（如Apache、Nginx、IIS......）
* Node.js代码处理请求的逻辑
* Node.js代码负责Web服务器的各种“配置”

使用Node.js核心模块http创建Web服务器<br>
cd /home/test/<br>
mkdir p8<br>
cd p8/<br>
ll<br>

cd ..<br>
mv p8/ part8<br>
cd part8<br>

web.js
```
var http = require('http');

var requestHandler = function(req, res) {
    res.end('hello');
};

var web = http.createServer(requestHandler);

web.listen(18000);

console.log('http running on http://localhost:18000');
```
node web.js<br>
curl http://localhost:18000