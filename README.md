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
    receiver: 'http://<host>:8999/receiver',
    //远端目录
    to: '/home/fis/www/'
  })
})
```
