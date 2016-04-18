receiver
========

FIS receiver on node.js

### use

```bash
$ git clone https://github.com/fex-team/receiver.git
$ cd receiver
$ npm install
$ node server.js # default port 8999, use `node server.js <port>` change port
```

_fis-conf.js_

```javascript
fis.config.merge({
    deploy: {
        remote: {
            receiver: 'http://<host>:8999/receiver',
            from: '/public',
            //远端目录
            to: '/home/fis/www/'
        }
    }
});
```

fis3 中配置方式。

```js
fis.match('*', {
  deploy: fis.plugin('http-push', {
    receiver: 'http://cq.01.p.p.baidu.com:8888/receiver.php',
    to: '/home/work/htdocs' // 注意这个是指的是测试机器的路径，而非本地机器
  })
})
```
