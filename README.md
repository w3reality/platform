# w3reality-sdk.js
(WIP) no public releases available yet

## Demos

### Open source VR websites

- minigame - A fully playable 3D game.  Can you reach the top floor where a surprising prize is awaiting you ;) ([🔥live](https://w3reality.com/visit?v=_github&o=w3reality&r=sdk-example-minigame&m=umd) | [source](https://github.com/w3reality/sdk-example-minigame))
- genesis - A minimal implementation. ([live](https://w3reality.com/visit?v=_github&o=w3reality&r=genesis) | [source](https://github.com/w3reality/genesis/blob/master/src/index.js))
- esm module loading - A pedantic example of using custom ES modules. ([live](https://w3reality.com/visit?v=_github&o=w3reality&r=sdk-example-esm) | [source](https://github.com/w3reality/sdk-example-esm))
- amd module loading - A pedantic example of using custom AMD modules. ([live](https://w3reality.com/visit?v=_github&o=w3reality&r=sdk-example-amd) | [source](https://github.com/w3reality/sdk-example-amd))

### Prototype VR websites in W3Reality

Many of our prototype/experimental websites (related to games, multimedia, dataviz, education) can be found in 🔥 https://w3reality.com/

## Usage

Here is a minimal VR website implementation using the `SDK.App` class:

``` js
const SDK = window.requirejs('w3reality-sdk');
const THREE = window.THREE;

class MyApp extends SDK.App {
    // override
    static async fetchAssets() {
        return null;
    }

    // override
    static createWorld(assets=null) {
        return SDK.App.createWorld();
    }

    // override
    constructor(data, name='myapp') {
        super(data, name);
        const scene = new THREE.Scene();
        // ... (construct and add THREE objects to scene)
        this.setScene(scene);
    }

    // override
    update(t, dt) {
        super.update(t, dt);
        // ... (implement the dynamic logic)
    }

    // override
    free() {
        super.free();
        // ... (free custom resources if any)
    }
}

export default MyApp;
```

## API
(WIP)
