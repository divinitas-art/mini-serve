<div></div>

# flickserve 🍛

Ultralight http server with live reload.  
<sub><code>CLI + API</code></sub>

<br>

This is fork of [nativew/serve](https://github.com/nativew/serve). I missed fallback option usefull for apps with react router

<br>

### Simple CLI and API

### With live reload

### Light and modern

### No dependencies

<br>

### One command

```zsh
npm init flickserve
```

<br>

### Or one function

```js
import flickserve from 'flickserve';

flickserve.start();
```

<br>

### To start 🍛

<br>

### CLI

By default, it serves `public` if the folder exists, otherwise root `/`.  
Or you can specify a different folder.

```zsh
npm init flickserve [folder]
```

<br>

### API

```js
import flickserve from 'flickserve';

flickserve.start({
    port: 7000,
    root: '.',
    fallback: undefined, // set to "index.html", great for react router etc.
    live: true
});
```

<br>

### Live reload

```js
serve.update();
```

<br>

### Use any file watcher

<br>

[Chokidar](https://github.com/paulmillr/chokidar)

```js
import flickserve from 'flickserve';
import chokidar from 'chokidar';

flickserve.start();

chokidar.watch('.').on('change', () => {
    flickserve.update();
});
```

<br>

[esbuild](https://esbuild.github.io/api/#watch)

Use the official wrapper for esbuild's watch &nbsp; → &nbsp; [esbuild-serve](https://github.com/divinitas-art/esbuild-serve)

<br>

### Log

Import the util functions to log updates with colours.

```js
import flickserve, { error, log } from 'flickserve';

flickserve.update();

hasError
    ? error('× Failed') // Red
    : log('✓ Updated'); // Green
```

<br><br>

<div></div>
