ss-engine.io
============

Engine.io websocket transport layer for SocketStream

Installation
---

    npm install ss-engine.io

Usage
---

In your SocketStream application's app file, insert the following line of code:

    ss.ws.transport.use(require('ss-engine.io'));

By default, the library assumes that you are running your SocketStream app on port 3000. If you are running it on another port, you can configure it like this:

    ss.ws.transport.use(require('ss-engine.io'), {client:{host:'localhost', port:1337}});

Tests
---

    make test
 
License & Credits
---

2012 Anephenix Ltd. Ss-engine.io is licensed under the MIT License.