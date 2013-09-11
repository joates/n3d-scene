## n3d-scene (0.0.1-alpha)

A **plugin module** which provides a 3D rendering context (for use with [n3d-gamecore](https://github.com/joates/n3d-gamecore))
This code _does NOT do anything_ on it's own, it's not supposed to !!
Please also read the documentation for n3d-gamecore [here](https://github.com/joates/n3d-gamecore/tree/dev)

#### API
* a plugin module _must_ export an `object` which has either a `client` property, a `server` property OR _both_

for example:
```javascript
PluginClient = function() {
  // do some client-side stuff.
}

PluginServer = function() {
  // do some stuff on the server.
}

module.exports = {
  client:  PluginClient,
  server:  PluginServer,
  options: {},  /* none */
  weight:  0    /* default */
}
```

* `options  /* TODO: */`
* `weight   /* TODO: */`
* PluginClient should include an `init` method which will be automatically called when the game finishes initialising.
* Other _events_ that a plugin can register listeners for (in it's own `init` method) are `update` and `render` (others may be added in future as the API development progresses)

