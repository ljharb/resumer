# resumer

Pause a stream resume it immediately on the next tick unless somebody called
`.pause()`.

This module has the same signature as
[through](https://npmjs.com/package/through).

# example

``` js
var resumer = require('resumer');
createStream().pipe(process.stdout);

function createStream () {
    var stream = resumer();
    stream.queue('beep boop\n');
    return stream;
}
```

```
$ node example/resume.js
beep boop
```

# methods

# install

With [npm](https://npmjs.org) do:

```
npm install resumer
```

# license

MIT
