node-snowflake
==============

node-snowflake is a node.js clone for [twitter snowflake](https://github.com/twitter/snowflake).

## How to use

```js
// only run simple http server
require('node-snowflake').Server(3001);
```

```sh
curl http://localhost:3001/next_id?worker_id={optional}&data_center_id={optional}&sequence={optional}

# response : {"id":"439658373735124992"}
```

--------------------------

```js
// only run snowflake nextId
var snowflake = require('node-snowflake').Snowflake;
var id = snowflake.nextId(); // use default set<br>

// or

snowflake.init({worker_id : 1, data_center_id : 1, sequence : 0});
var id = snowflake.nextId();

console.log(id);
```

> See examples/example.js
