# w3reality-sdk.js
(WIP) no public releases available yet

## Usage

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

## Examples
