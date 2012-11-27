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

Debugging
---

Engine.IO uses the VisionMedia [debug module](https://github.com/visionmedia/debug). To debug connection issues, you must 

* enable `client.debug` in the `ss.ws.transport.use` options (`ss.ws.transport.use(ss_eio,{client:{debug:true}})`).
* set the `DEBUG` environment variable to `engine*`, or, in your app, set `process.env.DEBUG` accordingly, before requiring `ss-engine.io`. If you want to limit the type of message, you can be more precise, and specify a comma separated list. For example:
    
    process.env.DEBUG = "engine:socket,engine:ws"

You can get the various categories by watching the `engine*` log.

Your browser must support `localStorage` for the debug mode to work. That means IE8+, and recent-ish Firefox, Chrome, Safari and Opera. 

Note that on the client side, when `client.debug` is `true`, the `localStorage.debug` slot will be mutated. It treats the `debug` value as a CSV list, and add or removes `engine*` entries according to the current mode. This should be benign in most cases.

When client.debug is not set (the default), nothing happens.

Tests
---

    make test
 
License & Credits
---

2012 Anephenix Ltd. Ss-engine.io is licensed under the MIT License.