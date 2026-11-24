# Changes

## 4.0.0 2026-11-20

First entry of this change log. Earlier versions are on npm and in the git history.

* Seneca 4: the peer dependency is `seneca` `^4.0.0` (was `>=3||>=4.0.0-rc2`).
  Seneca 3 users stay on `@seneca/entity-util@3`.
* The entity peer dependency is `@seneca/entity` `^29.0.0` (was `seneca-entity`
  `>=27`). A peer dependency on `seneca-entity` made npm install seneca-entity 28,
  which stops a Seneca 4 process at startup with `plugin_gubu_shape`. Load the
  entity plugin by its full name: `seneca.use('@seneca/entity')`.
* The `seneca-promisify` peer dependency is removed. Seneca 4 has it built in;
  do not call `use('promisify')` (D4).
* Node.js 24 or later (`engines.node` `>=24`).
* The plugin code and options are unchanged.
* `package.json` lists the shipped `files`, names the `types`, and points
  `repository`, `bugs` and `homepage` at `senecajs/seneca-entity-util`.
* Tests load `@seneca/entity` by full name and run with `@hapi/lab` 25 on
  Seneca 4.0.0 and `seneca-plugin-validator` 0.7.0. The test override of
  `role:entity,cmd:save` is written as `sys:entity,cmd:save`.
* The `doc` script and the `@seneca/doc` development dependency are removed. The
  tests do not use it, and the README sections it generated are kept as they are.
  The unused `coveralls`, `lab-transform-typescript` and `.travis.yml` are removed.
