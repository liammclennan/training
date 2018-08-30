Import & Export
============

The import statement is used to import bindings which are exported by another module. 

Read the MDN documention for [import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and [export](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export).

Import everything
-----------

```javascript
import * as Foo from './foo';
```

Import selectively
-------------

```javascript
import {sum, find} from 'lodash';
```

Import the default export
----------

```javascript
import whatever from 'whatever';
```