# @seneca/entity-util

[![Npm][BadgeNpm]][Npm]


Utilities for [Seneca](senecajs.org) entities.

* rtag: random revision tags generated per save; provides support for complex object caching.
* archive: archival of deleted entities.
* when: injection of created and modified time stamps
* duration: injection of entity action duration times in results as meta data



## Install

Version 4 requires Seneca 4 and `@seneca/entity` 29 (Node.js 24 or later).
Seneca 3 users stay on `@seneca/entity-util@3`.

```sh
$ npm install seneca@^4 @seneca/entity @seneca/entity-util
```

```js
const Seneca = require('seneca')

const seneca = Seneca()
  .use('@seneca/entity')
  .use('@seneca/entity-util', { rtag: { active: true } })
```


<!--START:options-->


## Options

* `rtag` : object
* `when` : object
* `duration` : object
* `archive` : object
* `derive` : object
* `errors` : object
* `init$` : boolean


<!--END:options-->



<!--START:action-list-->


## Action Patterns

* [role:cache,resolve:rtag](#-rolecacheresolvertag-)
* [role:cache,stats:rtag](#-rolecachestatsrtag-)
* [sys:entity,cmd:list](#-sysentitycmdlist-)
* [sys:entity,cmd:load](#-sysentitycmdload-)
* [sys:entity,cmd:remove](#-sysentitycmdremove-)
* [sys:entity,cmd:save](#-sysentitycmdsave-)
* [sys:entity,derive:add](#-sysentityderiveadd-)
* [sys:entity,derive:list](#-sysentityderivelist-)


<!--END:action-list-->

<!--START:action-desc-->


## Action Descriptions

### &laquo; `role:cache,resolve:rtag` &raquo;

Use rtag to load cached version of expensive result.



----------
### &laquo; `role:cache,stats:rtag` &raquo;

Get rtag cache usage statistics.



----------
### &laquo; `sys:entity,cmd:list` &raquo;

No description provided.



----------
### &laquo; `sys:entity,cmd:load` &raquo;

No description provided.



----------
### &laquo; `sys:entity,cmd:remove` &raquo;

No description provided.



----------
### &laquo; `sys:entity,cmd:save` &raquo;

Override sys:entity,cmd:save to apply utilities.



----------
### &laquo; `sys:entity,derive:add` &raquo;

No description provided.



----------
### &laquo; `sys:entity,derive:list` &raquo;

No description provided.



----------


<!--END:action-desc-->


[BadgeNpm]: https://badge.fury.io/js/%40seneca%2Fentity-util.svg
[Npm]: https://www.npmjs.com/package/@seneca/entity-util
