本课时主要内容如下：
* 简单的Express服务器

yum install npm<br>
wget http://npmjs.org/install.sh<br>
sh install.sh<br>
npm --version<br>
npm install express<br>
express.js
```
var express = require('express');

var app = express();

app.use(express.static('./public'));

app.get('/', function(req, res) {
    res.end('hello\n');
});

var Router = express.Router();

Router.get('/add', function(req, res){
    res.end('Router /add\n');
});

Router.get('/list', function(req, res){
    res.end('Router /list\n');
});

app.use('/post', Router);

app.listen(18001, function afterListen() {
    console.log('express running on http://localhost:18001');
});
```
node express.js<br>
curl http://localhost:18001

npm install -g express-generator<br>
express expressHello<br>
cd expressHello/<br>
ll<br>
vim package.json<br>
npm install<br>
node bin/www<br>
curl http://localhost:3000<br>

* 静态文件服务器

    静态文件范围：
    * 网页
    * 纯文本
    * 图片
    * 前端JavaScript代码
    * CSS样式表文件
    * 媒体文件
    * 字体文件

    使用Express创建静态文件服务器<br>
    curl http://localhost:18001/test.txt<br>

* 路由
    http://7te9fe.com1.z0.glb.clouddn.com/shanghai-insect-museum_P50101-142628-001.jpg<br>
    http://chensd.com/2015-01/45-useful-javascript-tips-tricks-and-best-practices.html<br>
    http://php.net/downloads.php<br>
    http://example.com/user/login.jsp?source=chrome&from=google_ncr<br>
    http://example.com/user/docs.php#intro/section1<br>

    https://v2ex.com/mission/daily<br>

    * 将不同的请求，分配给相应的处理函数
    * 区分：路径、请求方法
* 中间件
