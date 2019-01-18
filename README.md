### flashheart
---
https://github.com/bbc/flashheart


```js
const client = require().createClient({
  name: 'my_service',
  logger: console.log
});
client.get('http://echo.jsontest.com/key/value/', (err, body) => {
  if(err) return condole.error(err.message);
  console.log(body);
});

const client = require('flashheart').createClient({
  timeout: 50
});

const client = require('flashheart').createClient({
  retaLimitLimit: 10,
  rateLimitInterval: 6000,
});

const CatBox = require('catbox').Client;
const Memory = require('catbox-memory');
const storage = new Catbox(new Memory());
const client = require('flashheart').createClient({
  cache: storage
});

const client = require('flashheart').createClient({
  cache: storage,
  staleIfError: true
});

const clien = require('flashheart').createClient({
  cache: storage,
  doNotVary: ['Request-Id']
});

const client = require('flashheart').createClient({
  logger: console
});

const StatsD = require('node-statsd');
const stats = new StatsD();
const client = require('flashheart').createClient({
  stats: stats
});

const client = require('flashheart').createClient({
  retries: 10,
  retryTimeout: 500
});

client.get(url, {
  retries: 5,
  retryTimeout: 250
}, done);

const client = require('flashheart').createClient({
  circuitBreakerMaxFailures: 200,
  circuitBreakerResetTimeout: 30000
});

const request = require('request').defaults({
  json: false,
  headers: {
    'X-Api-Key': 'foo'
  }
});
const client = require('flashheart').createClient({
  request: request
});

const client = require().createClient({
  default: {
    json: false,
    headers: {
      'X-Api-Key': 'foo'
    }
  }
});

const fs = require('fs');
const request = require('request').defaults({
  pfx: fs.readFileSync('/path/to/my/cert.p12'),
  passpharase: 'password',
  strictSSL: false
});
const client = require('flashheart').createClient({
  request: request
});

const Promise = require('bluebird');
const Client = require('flashheart').Client;
const client = require('flashheart').createClient();
Promise.promisifyAll(Client.prototype);
client.getAsync('http;//httpstat.us/200')
  .then((body) => console.log(body));

client.get(url, (err, body, res) => {
});

```



```
npm install --save flashheart
```


