receiver
========

FIS receiver on node.js

### use

```bash
$ git clone https://github.com/fex-team/receiver.git
$ cd receiver
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
