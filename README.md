# api documentation for  [thinky (v2.3.8)](https://github.com/neumino/thinky#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-thinky.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-thinky) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-thinky.svg)](https://travis-ci.org/npmdoc/node-npmdoc-thinky)
#### RethinkDB ORM for Node.js

[![NPM](https://nodei.co/npm/thinky.png?downloads=true)](https://www.npmjs.com/package/thinky)

[![apidoc](https://npmdoc.github.io/node-npmdoc-thinky/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-thinky_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-thinky/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-thinky/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-thinky/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Michel Tu",
        "email": "orphee@gmail.com",
        "url": "http://justonepixel.com/"
    },
    "bugs": {
        "url": "https://github.com/neumino/thinky/issues"
    },
    "dependencies": {
        "bluebird": "~2.10.2",
        "rethinkdbdash": "~2.3.0",
        "validator": "~3.22.1"
    },
    "description": "RethinkDB ORM for Node.js",
    "devDependencies": {
        "mocha": "~1.21.5"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "4d3d01fe0aaaa8cd97276965f40dbb4f017300f3",
        "tarball": "https://registry.npmjs.org/thinky/-/thinky-2.3.8.tgz"
    },
    "gitHead": "7967e52f5f00ad2762edab98351da1fa9629972d",
    "homepage": "https://github.com/neumino/thinky#readme",
    "keywords": [
        "rethinkdb",
        "orm"
    ],
    "license": "MIT",
    "main": "lib/thinky.js",
    "maintainers": [
        {
            "name": "neumino",
            "email": "orphee@gmail.com"
        }
    ],
    "name": "thinky",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/neumino/thinky.git"
    },
    "scripts": {
        "test": "mocha --check-leaks -t 20000"
    },
    "version": "2.3.8"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module thinky](#apidoc.module.thinky)
1.  [function <span class="apidocSignatureSpan">thinky.</span>document (model, options)](#apidoc.element.thinky.document)
1.  [function <span class="apidocSignatureSpan">thinky.</span>feed (feed, model)](#apidoc.element.thinky.feed)
1.  [function <span class="apidocSignatureSpan">thinky.</span>model (name, schema, options, thinky)](#apidoc.element.thinky.model)
1.  [function <span class="apidocSignatureSpan">thinky.</span>query (model, query, options, error)](#apidoc.element.thinky.query)
1.  object <span class="apidocSignatureSpan">thinky.</span>document.prototype
1.  object <span class="apidocSignatureSpan">thinky.</span>errors
1.  object <span class="apidocSignatureSpan">thinky.</span>feed.prototype
1.  object <span class="apidocSignatureSpan">thinky.</span>model.prototype
1.  object <span class="apidocSignatureSpan">thinky.</span>query.prototype
1.  object <span class="apidocSignatureSpan">thinky.</span>schema
1.  object <span class="apidocSignatureSpan">thinky.</span>type
1.  object <span class="apidocSignatureSpan">thinky.</span>util

#### [module thinky.document](#apidoc.module.thinky.document)
1.  [function <span class="apidocSignatureSpan">thinky.</span>document (model, options)](#apidoc.element.thinky.document.document)

#### [module thinky.document.prototype](#apidoc.module.thinky.document.prototype)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>__makeSavableCopy (doc, schema, options, model, r)](#apidoc.element.thinky.document.prototype.__makeSavableCopy)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_batchSave (executeInsert)](#apidoc.element.thinky.document.prototype._batchSave)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_batchSaveSelf (executeInsert)](#apidoc.element.thinky.document.prototype._batchSaveSelf)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_delete (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback)](#apidoc.element.thinky.document.prototype._delete)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_deleteHook (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback)](#apidoc.element.thinky.document.prototype._deleteHook)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_emitRetrieve ()](#apidoc.element.thinky.document.prototype._emitRetrieve)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_generateDefault ()](#apidoc.element.thinky.document.prototype._generateDefault)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getModel ()](#apidoc.element.thinky.document.prototype._getModel)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getOptions ()](#apidoc.element.thinky.document.prototype._getOptions)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getSchemaOptions ()](#apidoc.element.thinky.document.prototype._getSchemaOptions)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getVirtual ()](#apidoc.element.thinky.document.prototype._getVirtual)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_makeSavableCopy ()](#apidoc.element.thinky.document.prototype._makeSavableCopy)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_merge (obj)](#apidoc.element.thinky.document.prototype._merge)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_onSaved (result, docToSave, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._onSaved)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_onSavedBelongsTo ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._onSavedBelongsTo)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_save (docToSave, saveAll, savedModel, callback)](#apidoc.element.thinky.document.prototype._save)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveHook (docToSave, saveAll, savedModel)](#apidoc.element.thinky.document.prototype._saveHook)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveLinks (docToSave, saveAll, resolve, reject)](#apidoc.element.thinky.document.prototype._saveLinks)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveMany (docToSave, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._saveMany)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveSelf ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._saveSelf)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveVirtual ()](#apidoc.element.thinky.document.prototype._saveVirtual)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setFeed (feed)](#apidoc.element.thinky.document.prototype._setFeed)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setOldValue (value)](#apidoc.element.thinky.document.prototype._setOldValue)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setUnSaved ()](#apidoc.element.thinky.document.prototype._setUnSaved)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_validateHook (options, modelToValidate, validateAll, validatedModel, prefix)](#apidoc.element.thinky.document.prototype._validateHook)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_validateIsAsync (modelToValidate, validateAll, validatedModel)](#apidoc.element.thinky.document.prototype._validateIsAsync)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>addRelation ()](#apidoc.element.thinky.document.prototype.addRelation)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>closeFeed ()](#apidoc.element.thinky.document.prototype.closeFeed)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>delete (callback)](#apidoc.element.thinky.document.prototype.delete)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>deleteAll (docToDelete, callback)](#apidoc.element.thinky.document.prototype.deleteAll)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>generateVirtualValues ()](#apidoc.element.thinky.document.prototype.generateVirtualValues)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getFeed ()](#apidoc.element.thinky.document.prototype.getFeed)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getModel ()](#apidoc.element.thinky.document.prototype.getModel)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getOldValue ()](#apidoc.element.thinky.document.prototype.getOldValue)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>isSaved ()](#apidoc.element.thinky.document.prototype.isSaved)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>merge (obj)](#apidoc.element.thinky.document.prototype.merge)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>purge (callback)](#apidoc.element.thinky.document.prototype.purge)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>removeRelation ()](#apidoc.element.thinky.document.prototype.removeRelation)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>save (callback)](#apidoc.element.thinky.document.prototype.save)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>saveAll (docToSave, callback)](#apidoc.element.thinky.document.prototype.saveAll)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>setSaved (all)](#apidoc.element.thinky.document.prototype.setSaved)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>validate (options, modelToValidate, validateAll, validatedModel, prefix)](#apidoc.element.thinky.document.prototype.validate)
1.  [function <span class="apidocSignatureSpan">thinky.document.prototype.</span>validateAll (options, modelToValidate)](#apidoc.element.thinky.document.prototype.validateAll)

#### [module thinky.errors](#apidoc.module.thinky.errors)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>DocumentNotFound (message)](#apidoc.element.thinky.errors.DocumentNotFound)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>DuplicatePrimaryKey (message, primaryKey)](#apidoc.element.thinky.errors.DuplicatePrimaryKey)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>InvalidWrite (message, raw)](#apidoc.element.thinky.errors.InvalidWrite)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>ThinkyError ()](#apidoc.element.thinky.errors.ThinkyError)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>ValidationError (message)](#apidoc.element.thinky.errors.ValidationError)
1.  [function <span class="apidocSignatureSpan">thinky.errors.</span>create (errorOrMessage)](#apidoc.element.thinky.errors.create)
1.  object <span class="apidocSignatureSpan">thinky.errors.</span>DOCUMENT_NOT_FOUND_REGEX
1.  object <span class="apidocSignatureSpan">thinky.errors.</span>DUPLICATE_PRIMARY_KEY_REGEX

#### [module thinky.feed](#apidoc.module.thinky.feed)
1.  [function <span class="apidocSignatureSpan">thinky.</span>feed (feed, model)](#apidoc.element.thinky.feed.feed)

#### [module thinky.feed.prototype](#apidoc.module.thinky.feed.prototype)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_each (callback, onFinish)](#apidoc.element.thinky.feed.prototype._each)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_eachCb (err, data)](#apidoc.element.thinky.feed.prototype._eachCb)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_makeEmitter ()](#apidoc.element.thinky.feed.prototype._makeEmitter)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_next ()](#apidoc.element.thinky.feed.prototype._next)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>addListener ()](#apidoc.element.thinky.feed.prototype.addListener)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>close (callback)](#apidoc.element.thinky.feed.prototype.close)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>emit ()](#apidoc.element.thinky.feed.prototype.emit)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>listeners ()](#apidoc.element.thinky.feed.prototype.listeners)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>on ()](#apidoc.element.thinky.feed.prototype.on)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>once ()](#apidoc.element.thinky.feed.prototype.once)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>removeAllListeners ()](#apidoc.element.thinky.feed.prototype.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>removeListener ()](#apidoc.element.thinky.feed.prototype.removeListener)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>setMaxListeners ()](#apidoc.element.thinky.feed.prototype.setMaxListeners)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>toArray ()](#apidoc.element.thinky.feed.prototype.toArray)
1.  [function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>toString ()](#apidoc.element.thinky.feed.prototype.toString)

#### [module thinky.model](#apidoc.module.thinky.model)
1.  [function <span class="apidocSignatureSpan">thinky.</span>model (name, schema, options, thinky)](#apidoc.element.thinky.model.model)
1.  [function <span class="apidocSignatureSpan">thinky.model.</span>new (name, schema, options, thinky)](#apidoc.element.thinky.model.new)
1.  [function <span class="apidocSignatureSpan">thinky.model.</span>super_ ()](#apidoc.element.thinky.model.super_)

#### [module thinky.model.prototype](#apidoc.module.thinky.model.prototype)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ISO8601 ()](#apidoc.element.thinky.model.prototype.ISO8601)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_createIndex (name, fn, opts)](#apidoc.element.thinky.model.prototype._createIndex)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_get ()](#apidoc.element.thinky.model.prototype._get)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_getModel ()](#apidoc.element.thinky.model.prototype._getModel)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_parse (data, ungroup)](#apidoc.element.thinky.model.prototype._parse)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_promisesReady ()](#apidoc.element.thinky.model.prototype._promisesReady)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_setError (error)](#apidoc.element.thinky.model.prototype._setError)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_waitFor (promise)](#apidoc.element.thinky.model.prototype._waitFor)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>add ()](#apidoc.element.thinky.model.prototype.add)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>and ()](#apidoc.element.thinky.model.prototype.and)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>append ()](#apidoc.element.thinky.model.prototype.append)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>april ()](#apidoc.element.thinky.model.prototype.april)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>args ()](#apidoc.element.thinky.model.prototype.args)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>asc ()](#apidoc.element.thinky.model.prototype.asc)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>august ()](#apidoc.element.thinky.model.prototype.august)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>avg ()](#apidoc.element.thinky.model.prototype.avg)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>belongsTo (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.belongsTo)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>between ()](#apidoc.element.thinky.model.prototype.between)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>binary ()](#apidoc.element.thinky.model.prototype.binary)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>bracket ()](#apidoc.element.thinky.model.prototype.bracket)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>branch ()](#apidoc.element.thinky.model.prototype.branch)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>catch ()](#apidoc.element.thinky.model.prototype.catch)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ceil ()](#apidoc.element.thinky.model.prototype.ceil)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>changeAt ()](#apidoc.element.thinky.model.prototype.changeAt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>changes ()](#apidoc.element.thinky.model.prototype.changes)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>circle ()](#apidoc.element.thinky.model.prototype.circle)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>coerceTo ()](#apidoc.element.thinky.model.prototype.coerceTo)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>concatMap ()](#apidoc.element.thinky.model.prototype.concatMap)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>config ()](#apidoc.element.thinky.model.prototype.config)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>contains ()](#apidoc.element.thinky.model.prototype.contains)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>count ()](#apidoc.element.thinky.model.prototype.count)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>date ()](#apidoc.element.thinky.model.prototype.date)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>day ()](#apidoc.element.thinky.model.prototype.day)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dayOfWeek ()](#apidoc.element.thinky.model.prototype.dayOfWeek)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dayOfYear ()](#apidoc.element.thinky.model.prototype.dayOfYear)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>db ()](#apidoc.element.thinky.model.prototype.db)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbCreate ()](#apidoc.element.thinky.model.prototype.dbCreate)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbDrop ()](#apidoc.element.thinky.model.prototype.dbDrop)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbList ()](#apidoc.element.thinky.model.prototype.dbList)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>december ()](#apidoc.element.thinky.model.prototype.december)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>default ()](#apidoc.element.thinky.model.prototype.default)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>define (key, fn)](#apidoc.element.thinky.model.prototype.define)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>defineStatic (key, fn)](#apidoc.element.thinky.model.prototype.defineStatic)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>delay ()](#apidoc.element.thinky.model.prototype.delay)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>delete ()](#apidoc.element.thinky.model.prototype.delete)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>deleteAt ()](#apidoc.element.thinky.model.prototype.deleteAt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>desc ()](#apidoc.element.thinky.model.prototype.desc)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>difference ()](#apidoc.element.thinky.model.prototype.difference)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>distance ()](#apidoc.element.thinky.model.prototype.distance)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>distinct ()](#apidoc.element.thinky.model.prototype.distinct)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>div ()](#apidoc.element.thinky.model.prototype.div)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>do ()](#apidoc.element.thinky.model.prototype.do)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docAddListener (eventKey, listener)](#apidoc.element.thinky.model.prototype.docAddListener)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docListeners (eventKey, raw)](#apidoc.element.thinky.model.prototype.docListeners)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docOn (eventKey, listener)](#apidoc.element.thinky.model.prototype.docOn)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docOnce (eventKey, listener)](#apidoc.element.thinky.model.prototype.docOnce)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docRemoveAllListeners (ev)](#apidoc.element.thinky.model.prototype.docRemoveAllListeners)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docRemoveListener (ev, listener)](#apidoc.element.thinky.model.prototype.docRemoveListener)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docSetMaxListeners (n)](#apidoc.element.thinky.model.prototype.docSetMaxListeners)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>downcase ()](#apidoc.element.thinky.model.prototype.downcase)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>during ()](#apidoc.element.thinky.model.prototype.during)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ensureIndex (name, fn, opts)](#apidoc.element.thinky.model.prototype.ensureIndex)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>epochTime ()](#apidoc.element.thinky.model.prototype.epochTime)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>eq ()](#apidoc.element.thinky.model.prototype.eq)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>eqJoin ()](#apidoc.element.thinky.model.prototype.eqJoin)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>error ()](#apidoc.element.thinky.model.prototype.error)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>execute (options)](#apidoc.element.thinky.model.prototype.execute)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>expr ()](#apidoc.element.thinky.model.prototype.expr)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>february ()](#apidoc.element.thinky.model.prototype.february)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>fill ()](#apidoc.element.thinky.model.prototype.fill)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>filter ()](#apidoc.element.thinky.model.prototype.filter)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>finally ()](#apidoc.element.thinky.model.prototype.finally)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>floor ()](#apidoc.element.thinky.model.prototype.floor)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>fold ()](#apidoc.element.thinky.model.prototype.fold)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>forEach ()](#apidoc.element.thinky.model.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>friday ()](#apidoc.element.thinky.model.prototype.friday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ge ()](#apidoc.element.thinky.model.prototype.ge)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>geojson ()](#apidoc.element.thinky.model.prototype.geojson)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>get ()](#apidoc.element.thinky.model.prototype.get)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getAll ()](#apidoc.element.thinky.model.prototype.getAll)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getField ()](#apidoc.element.thinky.model.prototype.getField)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getIntersecting ()](#apidoc.element.thinky.model.prototype.getIntersecting)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getJoin ()](#apidoc.element.thinky.model.prototype.getJoin)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getNearest ()](#apidoc.element.thinky.model.prototype.getNearest)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getOptions ()](#apidoc.element.thinky.model.prototype.getOptions)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getTableName ()](#apidoc.element.thinky.model.prototype.getTableName)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>grant ()](#apidoc.element.thinky.model.prototype.grant)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>group ()](#apidoc.element.thinky.model.prototype.group)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>gt ()](#apidoc.element.thinky.model.prototype.gt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasAndBelongsToMany (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasAndBelongsToMany)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasFields ()](#apidoc.element.thinky.model.prototype.hasFields)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasMany (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasMany)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasOne (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasOne)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hours ()](#apidoc.element.thinky.model.prototype.hours)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>http ()](#apidoc.element.thinky.model.prototype.http)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>inTimezone ()](#apidoc.element.thinky.model.prototype.inTimezone)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>includes ()](#apidoc.element.thinky.model.prototype.includes)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexCreate ()](#apidoc.element.thinky.model.prototype.indexCreate)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexDrop ()](#apidoc.element.thinky.model.prototype.indexDrop)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexList ()](#apidoc.element.thinky.model.prototype.indexList)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexRename ()](#apidoc.element.thinky.model.prototype.indexRename)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexStatus ()](#apidoc.element.thinky.model.prototype.indexStatus)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexWait ()](#apidoc.element.thinky.model.prototype.indexWait)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexesOf ()](#apidoc.element.thinky.model.prototype.indexesOf)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>info ()](#apidoc.element.thinky.model.prototype.info)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>innerJoin ()](#apidoc.element.thinky.model.prototype.innerJoin)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>insert ()](#apidoc.element.thinky.model.prototype.insert)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>insertAt ()](#apidoc.element.thinky.model.prototype.insertAt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>intersects ()](#apidoc.element.thinky.model.prototype.intersects)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>isEmpty ()](#apidoc.element.thinky.model.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>january ()](#apidoc.element.thinky.model.prototype.january)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>js ()](#apidoc.element.thinky.model.prototype.js)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>json ()](#apidoc.element.thinky.model.prototype.json)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>july ()](#apidoc.element.thinky.model.prototype.july)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>june ()](#apidoc.element.thinky.model.prototype.june)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>keys ()](#apidoc.element.thinky.model.prototype.keys)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>le ()](#apidoc.element.thinky.model.prototype.le)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>limit ()](#apidoc.element.thinky.model.prototype.limit)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>line ()](#apidoc.element.thinky.model.prototype.line)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>literal ()](#apidoc.element.thinky.model.prototype.literal)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>lt ()](#apidoc.element.thinky.model.prototype.lt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>map ()](#apidoc.element.thinky.model.prototype.map)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>march ()](#apidoc.element.thinky.model.prototype.march)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>match ()](#apidoc.element.thinky.model.prototype.match)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>max ()](#apidoc.element.thinky.model.prototype.max)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>maxval ()](#apidoc.element.thinky.model.prototype.maxval)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>may ()](#apidoc.element.thinky.model.prototype.may)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>merge ()](#apidoc.element.thinky.model.prototype.merge)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>min ()](#apidoc.element.thinky.model.prototype.min)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>minutes ()](#apidoc.element.thinky.model.prototype.minutes)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>minval ()](#apidoc.element.thinky.model.prototype.minval)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>mod ()](#apidoc.element.thinky.model.prototype.mod)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>monday ()](#apidoc.element.thinky.model.prototype.monday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>month ()](#apidoc.element.thinky.model.prototype.month)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>mul ()](#apidoc.element.thinky.model.prototype.mul)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ne ()](#apidoc.element.thinky.model.prototype.ne)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>not ()](#apidoc.element.thinky.model.prototype.not)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>november ()](#apidoc.element.thinky.model.prototype.november)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>now ()](#apidoc.element.thinky.model.prototype.now)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>nth ()](#apidoc.element.thinky.model.prototype.nth)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>object ()](#apidoc.element.thinky.model.prototype.object)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>october ()](#apidoc.element.thinky.model.prototype.october)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>offsetsOf ()](#apidoc.element.thinky.model.prototype.offsetsOf)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>or ()](#apidoc.element.thinky.model.prototype.or)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>orderBy ()](#apidoc.element.thinky.model.prototype.orderBy)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>outerJoin ()](#apidoc.element.thinky.model.prototype.outerJoin)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>pluck ()](#apidoc.element.thinky.model.prototype.pluck)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>point ()](#apidoc.element.thinky.model.prototype.point)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>polygon ()](#apidoc.element.thinky.model.prototype.polygon)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>polygonSub ()](#apidoc.element.thinky.model.prototype.polygonSub)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>post (ev, fn)](#apidoc.element.thinky.model.prototype.post)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>pre (ev, fn)](#apidoc.element.thinky.model.prototype.pre)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>prepend ()](#apidoc.element.thinky.model.prototype.prepend)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>random ()](#apidoc.element.thinky.model.prototype.random)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>range ()](#apidoc.element.thinky.model.prototype.range)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ready ()](#apidoc.element.thinky.model.prototype.ready)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>rebalance ()](#apidoc.element.thinky.model.prototype.rebalance)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>reconfigure ()](#apidoc.element.thinky.model.prototype.reconfigure)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>reduce ()](#apidoc.element.thinky.model.prototype.reduce)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>removeRelations (relationsToRemove)](#apidoc.element.thinky.model.prototype.removeRelations)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>replace ()](#apidoc.element.thinky.model.prototype.replace)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>round ()](#apidoc.element.thinky.model.prototype.round)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>row ()](#apidoc.element.thinky.model.prototype.row)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>run (options)](#apidoc.element.thinky.model.prototype.run)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sample ()](#apidoc.element.thinky.model.prototype.sample)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>saturday ()](#apidoc.element.thinky.model.prototype.saturday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>save (docs, options)](#apidoc.element.thinky.model.prototype.save)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>seconds ()](#apidoc.element.thinky.model.prototype.seconds)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>september ()](#apidoc.element.thinky.model.prototype.september)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setDifference ()](#apidoc.element.thinky.model.prototype.setDifference)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setInsert ()](#apidoc.element.thinky.model.prototype.setInsert)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setIntersection ()](#apidoc.element.thinky.model.prototype.setIntersection)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setUnion ()](#apidoc.element.thinky.model.prototype.setUnion)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>skip ()](#apidoc.element.thinky.model.prototype.skip)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>slice ()](#apidoc.element.thinky.model.prototype.slice)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>spliceAt ()](#apidoc.element.thinky.model.prototype.spliceAt)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>split ()](#apidoc.element.thinky.model.prototype.split)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>status ()](#apidoc.element.thinky.model.prototype.status)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sub ()](#apidoc.element.thinky.model.prototype.sub)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sum ()](#apidoc.element.thinky.model.prototype.sum)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sunday ()](#apidoc.element.thinky.model.prototype.sunday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sync ()](#apidoc.element.thinky.model.prototype.sync)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>table ()](#apidoc.element.thinky.model.prototype.table)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableCreate ()](#apidoc.element.thinky.model.prototype.tableCreate)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableDrop ()](#apidoc.element.thinky.model.prototype.tableDrop)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableList ()](#apidoc.element.thinky.model.prototype.tableList)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableReady ()](#apidoc.element.thinky.model.prototype.tableReady)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>then ()](#apidoc.element.thinky.model.prototype.then)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>thursday ()](#apidoc.element.thinky.model.prototype.thursday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>time ()](#apidoc.element.thinky.model.prototype.time)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>timeOfDay ()](#apidoc.element.thinky.model.prototype.timeOfDay)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>timezone ()](#apidoc.element.thinky.model.prototype.timezone)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toEpochTime ()](#apidoc.element.thinky.model.prototype.toEpochTime)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toGeojson ()](#apidoc.element.thinky.model.prototype.toGeojson)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toISO8601 ()](#apidoc.element.thinky.model.prototype.toISO8601)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toJSON ()](#apidoc.element.thinky.model.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toJsonString ()](#apidoc.element.thinky.model.prototype.toJsonString)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toStream ()](#apidoc.element.thinky.model.prototype.toStream)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toString ()](#apidoc.element.thinky.model.prototype.toString)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tuesday ()](#apidoc.element.thinky.model.prototype.tuesday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>typeOf ()](#apidoc.element.thinky.model.prototype.typeOf)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ungroup ()](#apidoc.element.thinky.model.prototype.ungroup)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>union ()](#apidoc.element.thinky.model.prototype.union)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>upcase ()](#apidoc.element.thinky.model.prototype.upcase)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>update ()](#apidoc.element.thinky.model.prototype.update)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>uuid ()](#apidoc.element.thinky.model.prototype.uuid)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>values ()](#apidoc.element.thinky.model.prototype.values)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>wait ()](#apidoc.element.thinky.model.prototype.wait)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>wednesday ()](#apidoc.element.thinky.model.prototype.wednesday)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>withFields ()](#apidoc.element.thinky.model.prototype.withFields)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>without ()](#apidoc.element.thinky.model.prototype.without)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>year ()](#apidoc.element.thinky.model.prototype.year)
1.  [function <span class="apidocSignatureSpan">thinky.model.prototype.</span>zip ()](#apidoc.element.thinky.model.prototype.zip)

#### [module thinky.query](#apidoc.module.thinky.query)
1.  [function <span class="apidocSignatureSpan">thinky.</span>query (model, query, options, error)](#apidoc.element.thinky.query.query)

#### [module thinky.query.prototype](#apidoc.module.thinky.query.prototype)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ISO8601 ()](#apidoc.element.thinky.query.prototype.ISO8601)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_convertGroupedData (data)](#apidoc.element.thinky.query.prototype._convertGroupedData)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_execute (options, parse)](#apidoc.element.thinky.query.prototype._execute)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_executeCallback (fullOptions, parse, groupFormat)](#apidoc.element.thinky.query.prototype._executeCallback)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_get ()](#apidoc.element.thinky.query.prototype._get)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_isPointWrite ()](#apidoc.element.thinky.query.prototype._isPointWrite)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_validateQueryResult (result)](#apidoc.element.thinky.query.prototype._validateQueryResult)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_validateUngroupResult (result)](#apidoc.element.thinky.query.prototype._validateUngroupResult)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>add ()](#apidoc.element.thinky.query.prototype.add)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>addRelation (field, joinedDocument)](#apidoc.element.thinky.query.prototype.addRelation)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>and ()](#apidoc.element.thinky.query.prototype.and)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>append ()](#apidoc.element.thinky.query.prototype.append)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>april ()](#apidoc.element.thinky.query.prototype.april)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>args ()](#apidoc.element.thinky.query.prototype.args)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>asc ()](#apidoc.element.thinky.query.prototype.asc)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>august ()](#apidoc.element.thinky.query.prototype.august)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>avg ()](#apidoc.element.thinky.query.prototype.avg)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>between ()](#apidoc.element.thinky.query.prototype.between)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>binary ()](#apidoc.element.thinky.query.prototype.binary)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bindExecute ()](#apidoc.element.thinky.query.prototype.bindExecute)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bindRun ()](#apidoc.element.thinky.query.prototype.bindRun)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bracket ()](#apidoc.element.thinky.query.prototype.bracket)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>branch ()](#apidoc.element.thinky.query.prototype.branch)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>catch ()](#apidoc.element.thinky.query.prototype.catch)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ceil ()](#apidoc.element.thinky.query.prototype.ceil)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>changeAt ()](#apidoc.element.thinky.query.prototype.changeAt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>changes ()](#apidoc.element.thinky.query.prototype.changes)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>circle ()](#apidoc.element.thinky.query.prototype.circle)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>coerceTo ()](#apidoc.element.thinky.query.prototype.coerceTo)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>concatMap ()](#apidoc.element.thinky.query.prototype.concatMap)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>config ()](#apidoc.element.thinky.query.prototype.config)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>contains ()](#apidoc.element.thinky.query.prototype.contains)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>count ()](#apidoc.element.thinky.query.prototype.count)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>date ()](#apidoc.element.thinky.query.prototype.date)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>day ()](#apidoc.element.thinky.query.prototype.day)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dayOfWeek ()](#apidoc.element.thinky.query.prototype.dayOfWeek)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dayOfYear ()](#apidoc.element.thinky.query.prototype.dayOfYear)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>db ()](#apidoc.element.thinky.query.prototype.db)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbCreate ()](#apidoc.element.thinky.query.prototype.dbCreate)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbDrop ()](#apidoc.element.thinky.query.prototype.dbDrop)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbList ()](#apidoc.element.thinky.query.prototype.dbList)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>december ()](#apidoc.element.thinky.query.prototype.december)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>default ()](#apidoc.element.thinky.query.prototype.default)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>delay ()](#apidoc.element.thinky.query.prototype.delay)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>delete ()](#apidoc.element.thinky.query.prototype.delete)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>deleteAt ()](#apidoc.element.thinky.query.prototype.deleteAt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>desc ()](#apidoc.element.thinky.query.prototype.desc)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>difference ()](#apidoc.element.thinky.query.prototype.difference)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>distance ()](#apidoc.element.thinky.query.prototype.distance)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>distinct ()](#apidoc.element.thinky.query.prototype.distinct)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>div ()](#apidoc.element.thinky.query.prototype.div)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>do ()](#apidoc.element.thinky.query.prototype.do)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>downcase ()](#apidoc.element.thinky.query.prototype.downcase)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>during ()](#apidoc.element.thinky.query.prototype.during)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>epochTime ()](#apidoc.element.thinky.query.prototype.epochTime)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>eq ()](#apidoc.element.thinky.query.prototype.eq)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>eqJoin ()](#apidoc.element.thinky.query.prototype.eqJoin)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>error ()](#apidoc.element.thinky.query.prototype.error)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>execute (options, callback)](#apidoc.element.thinky.query.prototype.execute)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>expr ()](#apidoc.element.thinky.query.prototype.expr)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>february ()](#apidoc.element.thinky.query.prototype.february)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>fill ()](#apidoc.element.thinky.query.prototype.fill)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>filter ()](#apidoc.element.thinky.query.prototype.filter)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>finally ()](#apidoc.element.thinky.query.prototype.finally)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>floor ()](#apidoc.element.thinky.query.prototype.floor)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>fold ()](#apidoc.element.thinky.query.prototype.fold)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>forEach ()](#apidoc.element.thinky.query.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>friday ()](#apidoc.element.thinky.query.prototype.friday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ge ()](#apidoc.element.thinky.query.prototype.ge)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>geojson ()](#apidoc.element.thinky.query.prototype.geojson)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>get ()](#apidoc.element.thinky.query.prototype.get)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getAll ()](#apidoc.element.thinky.query.prototype.getAll)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getField ()](#apidoc.element.thinky.query.prototype.getField)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getIntersecting ()](#apidoc.element.thinky.query.prototype.getIntersecting)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getJoin (modelToGet, getAll, gotModel)](#apidoc.element.thinky.query.prototype.getJoin)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getNearest ()](#apidoc.element.thinky.query.prototype.getNearest)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>grant ()](#apidoc.element.thinky.query.prototype.grant)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>group ()](#apidoc.element.thinky.query.prototype.group)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>gt ()](#apidoc.element.thinky.query.prototype.gt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>hasFields ()](#apidoc.element.thinky.query.prototype.hasFields)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>hours ()](#apidoc.element.thinky.query.prototype.hours)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>http ()](#apidoc.element.thinky.query.prototype.http)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>inTimezone ()](#apidoc.element.thinky.query.prototype.inTimezone)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>includes ()](#apidoc.element.thinky.query.prototype.includes)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexCreate ()](#apidoc.element.thinky.query.prototype.indexCreate)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexDrop ()](#apidoc.element.thinky.query.prototype.indexDrop)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexList ()](#apidoc.element.thinky.query.prototype.indexList)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexRename ()](#apidoc.element.thinky.query.prototype.indexRename)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexStatus ()](#apidoc.element.thinky.query.prototype.indexStatus)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexWait ()](#apidoc.element.thinky.query.prototype.indexWait)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexesOf ()](#apidoc.element.thinky.query.prototype.indexesOf)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>info ()](#apidoc.element.thinky.query.prototype.info)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>innerJoin ()](#apidoc.element.thinky.query.prototype.innerJoin)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>insert ()](#apidoc.element.thinky.query.prototype.insert)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>insertAt ()](#apidoc.element.thinky.query.prototype.insertAt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>intersects ()](#apidoc.element.thinky.query.prototype.intersects)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>isEmpty ()](#apidoc.element.thinky.query.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>january ()](#apidoc.element.thinky.query.prototype.january)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>js ()](#apidoc.element.thinky.query.prototype.js)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>json ()](#apidoc.element.thinky.query.prototype.json)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>july ()](#apidoc.element.thinky.query.prototype.july)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>june ()](#apidoc.element.thinky.query.prototype.june)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>keys ()](#apidoc.element.thinky.query.prototype.keys)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>le ()](#apidoc.element.thinky.query.prototype.le)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>limit ()](#apidoc.element.thinky.query.prototype.limit)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>line ()](#apidoc.element.thinky.query.prototype.line)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>literal ()](#apidoc.element.thinky.query.prototype.literal)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>lt ()](#apidoc.element.thinky.query.prototype.lt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>map ()](#apidoc.element.thinky.query.prototype.map)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>march ()](#apidoc.element.thinky.query.prototype.march)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>match ()](#apidoc.element.thinky.query.prototype.match)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>max ()](#apidoc.element.thinky.query.prototype.max)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>maxval ()](#apidoc.element.thinky.query.prototype.maxval)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>may ()](#apidoc.element.thinky.query.prototype.may)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>merge ()](#apidoc.element.thinky.query.prototype.merge)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>min ()](#apidoc.element.thinky.query.prototype.min)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>minutes ()](#apidoc.element.thinky.query.prototype.minutes)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>minval ()](#apidoc.element.thinky.query.prototype.minval)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>mod ()](#apidoc.element.thinky.query.prototype.mod)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>monday ()](#apidoc.element.thinky.query.prototype.monday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>month ()](#apidoc.element.thinky.query.prototype.month)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>mul ()](#apidoc.element.thinky.query.prototype.mul)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ne ()](#apidoc.element.thinky.query.prototype.ne)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>not ()](#apidoc.element.thinky.query.prototype.not)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>november ()](#apidoc.element.thinky.query.prototype.november)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>now ()](#apidoc.element.thinky.query.prototype.now)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>nth ()](#apidoc.element.thinky.query.prototype.nth)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>object ()](#apidoc.element.thinky.query.prototype.object)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>october ()](#apidoc.element.thinky.query.prototype.october)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>offsetsOf ()](#apidoc.element.thinky.query.prototype.offsetsOf)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>or ()](#apidoc.element.thinky.query.prototype.or)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>orderBy ()](#apidoc.element.thinky.query.prototype.orderBy)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>outerJoin ()](#apidoc.element.thinky.query.prototype.outerJoin)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>pluck ()](#apidoc.element.thinky.query.prototype.pluck)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>point ()](#apidoc.element.thinky.query.prototype.point)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>polygon ()](#apidoc.element.thinky.query.prototype.polygon)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>polygonSub ()](#apidoc.element.thinky.query.prototype.polygonSub)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>prepend ()](#apidoc.element.thinky.query.prototype.prepend)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>random ()](#apidoc.element.thinky.query.prototype.random)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>range ()](#apidoc.element.thinky.query.prototype.range)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>rebalance ()](#apidoc.element.thinky.query.prototype.rebalance)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>reconfigure ()](#apidoc.element.thinky.query.prototype.reconfigure)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>reduce ()](#apidoc.element.thinky.query.prototype.reduce)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>removeRelation (field, joinedDocument)](#apidoc.element.thinky.query.prototype.removeRelation)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>replace (value, options)](#apidoc.element.thinky.query.prototype.replace)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>round ()](#apidoc.element.thinky.query.prototype.round)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>row ()](#apidoc.element.thinky.query.prototype.row)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>run (options, callback)](#apidoc.element.thinky.query.prototype.run)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sample ()](#apidoc.element.thinky.query.prototype.sample)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>saturday ()](#apidoc.element.thinky.query.prototype.saturday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>seconds ()](#apidoc.element.thinky.query.prototype.seconds)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>september ()](#apidoc.element.thinky.query.prototype.september)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setDifference ()](#apidoc.element.thinky.query.prototype.setDifference)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setInsert ()](#apidoc.element.thinky.query.prototype.setInsert)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setIntersection ()](#apidoc.element.thinky.query.prototype.setIntersection)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setPointWrite ()](#apidoc.element.thinky.query.prototype.setPointWrite)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setPostValidation ()](#apidoc.element.thinky.query.prototype.setPostValidation)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setUnion ()](#apidoc.element.thinky.query.prototype.setUnion)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>skip ()](#apidoc.element.thinky.query.prototype.skip)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>slice ()](#apidoc.element.thinky.query.prototype.slice)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>spliceAt ()](#apidoc.element.thinky.query.prototype.spliceAt)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>split ()](#apidoc.element.thinky.query.prototype.split)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>status ()](#apidoc.element.thinky.query.prototype.status)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sub ()](#apidoc.element.thinky.query.prototype.sub)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sum ()](#apidoc.element.thinky.query.prototype.sum)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sunday ()](#apidoc.element.thinky.query.prototype.sunday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sync ()](#apidoc.element.thinky.query.prototype.sync)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>table ()](#apidoc.element.thinky.query.prototype.table)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableCreate ()](#apidoc.element.thinky.query.prototype.tableCreate)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableDrop ()](#apidoc.element.thinky.query.prototype.tableDrop)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableList ()](#apidoc.element.thinky.query.prototype.tableList)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>then ()](#apidoc.element.thinky.query.prototype.then)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>thursday ()](#apidoc.element.thinky.query.prototype.thursday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>time ()](#apidoc.element.thinky.query.prototype.time)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>timeOfDay ()](#apidoc.element.thinky.query.prototype.timeOfDay)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>timezone ()](#apidoc.element.thinky.query.prototype.timezone)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toEpochTime ()](#apidoc.element.thinky.query.prototype.toEpochTime)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toGeojson ()](#apidoc.element.thinky.query.prototype.toGeojson)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toISO8601 ()](#apidoc.element.thinky.query.prototype.toISO8601)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toJSON ()](#apidoc.element.thinky.query.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toJsonString ()](#apidoc.element.thinky.query.prototype.toJsonString)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toStream ()](#apidoc.element.thinky.query.prototype.toStream)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toString ()](#apidoc.element.thinky.query.prototype.toString)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tuesday ()](#apidoc.element.thinky.query.prototype.tuesday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>typeOf ()](#apidoc.element.thinky.query.prototype.typeOf)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ungroup ()](#apidoc.element.thinky.query.prototype.ungroup)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>union ()](#apidoc.element.thinky.query.prototype.union)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>upcase ()](#apidoc.element.thinky.query.prototype.upcase)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>update (value, options)](#apidoc.element.thinky.query.prototype.update)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>uuid ()](#apidoc.element.thinky.query.prototype.uuid)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>values ()](#apidoc.element.thinky.query.prototype.values)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>wait ()](#apidoc.element.thinky.query.prototype.wait)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>wednesday ()](#apidoc.element.thinky.query.prototype.wednesday)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>withFields ()](#apidoc.element.thinky.query.prototype.withFields)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>without ()](#apidoc.element.thinky.query.prototype.without)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>year ()](#apidoc.element.thinky.query.prototype.year)
1.  [function <span class="apidocSignatureSpan">thinky.query.prototype.</span>zip ()](#apidoc.element.thinky.query.prototype.zip)

#### [module thinky.schema](#apidoc.module.thinky.schema)
1.  [function <span class="apidocSignatureSpan">thinky.schema.</span>generateDefault (doc, defaultField, originalDoc)](#apidoc.element.thinky.schema.generateDefault)
1.  [function <span class="apidocSignatureSpan">thinky.schema.</span>generateVirtual (doc, defaultField, originalDoc, virtual)](#apidoc.element.thinky.schema.generateVirtual)
1.  [function <span class="apidocSignatureSpan">thinky.schema.</span>parse (schema, prefix, options, model)](#apidoc.element.thinky.schema.parse)
1.  [function <span class="apidocSignatureSpan">thinky.schema.</span>validate (doc, schema, prefix, options)](#apidoc.element.thinky.schema.validate)
1.  string <span class="apidocSignatureSpan">thinky.schema.</span>arrayPrefix

#### [module thinky.util](#apidoc.module.thinky.util)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>bindEmitter (self)](#apidoc.element.thinky.util.bindEmitter)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>changeProto (object, newProto)](#apidoc.element.thinky.util.changeProto)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>deepCopy (value)](#apidoc.element.thinky.util.deepCopy)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>extraField (prefix, key)](#apidoc.element.thinky.util.extraField)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>extractPrimaryKey (oldValue, newValue, primaryKey)](#apidoc.element.thinky.util.extractPrimaryKey)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>hook (options)](#apidoc.element.thinky.util.hook)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>isPlainObject (obj)](#apidoc.element.thinky.util.isPlainObject)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>loopKeys (obj, fn)](#apidoc.element.thinky.util.loopKeys)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>looseType (prefix, expected)](#apidoc.element.thinky.util.looseType)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>mergeOptions (options, newOptions)](#apidoc.element.thinky.util.mergeOptions)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>pseudoTypeError (type, missingField, prefix)](#apidoc.element.thinky.util.pseudoTypeError)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>recurse (key, joins, modelTo, all, done)](#apidoc.element.thinky.util.recurse)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>strictType (prefix, expected)](#apidoc.element.thinky.util.strictType)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>toArray (args)](#apidoc.element.thinky.util.toArray)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>tryCatch (toTry, handleError)](#apidoc.element.thinky.util.tryCatch)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>undefinedField (prefix)](#apidoc.element.thinky.util.undefinedField)
1.  [function <span class="apidocSignatureSpan">thinky.util.</span>validateIfUndefined (value, prefix, type, options)](#apidoc.element.thinky.util.validateIfUndefined)



# <a name="apidoc.module.thinky"></a>[module thinky](#apidoc.module.thinky)

#### <a name="apidoc.element.thinky.document"></a>[function <span class="apidocSignatureSpan">thinky.</span>document (model, options)](#apidoc.element.thinky.document)
- description and source-code
```javascript
function Document(model, options) {
  var self = this;  // Keep a reference to itself.

  this.constructor = model;  // The constructor for this model
  this._model = model._getModel(); // The instance of Model

  // We don't want to store options if they are different
  // than the one provided by the model
  if (util.isPlainObject(options)) {
    this._schemaOptions = {};
    this._schemaOptions.enforce_missing =
        (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
    this._schemaOptions.enforce_extra =
        (options.enforce_extra != null) ? options.enforce_extra : model.getOptions().enforce_extra;
    this._schemaOptions.enforce_type =
        (options.enforce_type != null) ? options.enforce_type : model.getOptions().enforce_type;
  }

  //TODO: We do not need to make a deep copy. We can do the same as for this._schemaOptions.
  options = options || {};
  this._options = {};
  this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : model.getOptions().timeFormat;
  this._options.validate = (options.validate != null) ? options.validate : model.getOptions().validate;

  this._saved = options.saved || false;  // Whether the document is saved or not

  util.bindEmitter(self);  // Copy methods from eventEmitter

  // links to hasOne/hasMany documents
  // We use it to know if some links have been removed/added before saving.
  // Example: { key: doc } or { key: [docs] }
  this._belongsTo = {};
  this._hasOne = {};
  this._hasMany = {};
  // Example: { <linkTableName>: { <valueOfRightKey>: true, ... }, ... }
  this._links = {}

  // Keep reference of any doc having a link pointing to this
  // So we can clean when users do doc.belongsToDoc.delete()
  this._parents = {
    _hasOne: {},      // <tableName>: [{doc, key}]
    _hasMany: {},     // <tableName>: [{doc, key}]
    _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
    _belongsLinks: {} // <tableName>: [{doc, key}]
  }

  // Bind listeners of the model to this documents.
  util.loopKeys(model._listeners, function(listeners, eventKey) {
    for(var j=0; j<listeners[eventKey].length; j++) {
      if (listeners[eventKey][j].once === false) {
        self.addListener(eventKey, listeners[eventKey][j].listener);
      }
      else if (listeners[eventKey][j].once === true) {
        self.once(eventKey, listeners[eventKey][j].listener);
      }
    }
  });


  // Atom feed
  this._active = false;
  this._feed = null;

  // Add customized methods of the model on this document.
  util.loopKeys(model._methods, function(methods, key) {
    if (self[key] === undefined) {
      self[key] = methods[key];
    }
    else {
      //TODO: Should we warn the users? Throw an error?
      console.log(self[key]);
      console.log("A property "+key+" is already defined in the prototype chain. Skipping.");
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed"></a>[function <span class="apidocSignatureSpan">thinky.</span>feed (feed, model)](#apidoc.element.thinky.feed)
- description and source-code
```javascript
function Feed(feed, model) {
  this.feed = feed;
  this.model = model;
  this._closed = false;

  this.each = this._each;
  this.next = this._next;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model"></a>[function <span class="apidocSignatureSpan">thinky.</span>model (name, schema, options, thinky)](#apidoc.element.thinky.model)
- description and source-code
```javascript
function Model(name, schema, options, thinky) {
<span class="apidocCodeCommentSpan">  /**
   * Name of the table used
   * @type {string}
   */
</span>  this._name = name;

  // We want a deep copy
  options = options || {};
  this._options = {};
  this._options.enforce_missing = (options.enforce_missing != null) ? options.enforce_missing : thinky._options.enforce_missing;
  this._options.enforce_extra = (options.enforce_extra != null) ? options.enforce_extra : thinky._options.enforce_extra;
  this._options.enforce_type = (options.enforce_type != null) ? options.enforce_type : thinky._options.enforce_type;
  this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : thinky._options.timeFormat;
  this._options.validate = (options.validate != null) ? options.validate : thinky._options.validate;

  this._schema = schemaUtil.parse(schema, '', this._options, this);
  //console.log(JSON.stringify(this._schema, null, 2));

  this.virtualFields = [];
  this.defaultFields = [];
  this._schema._getDefaultFields([], this.defaultFields, this.virtualFields)

  this.needToGenerateFields = (this.defaultFields.length+this.virtualFields.length) !== 0;

  this._pk = (options.pk != null) ? options.pk : 'id';

  this._table = (options.table != null) ? options.table : {};
  this._table.primaryKey = this._pk;

  this._thinky = thinky;

  this._validator = options.validator;

  this._indexes = {}; // indexName -> true
  this._pendingPromises = [];

  this._error = null; // If an error occured, we won't let people save things

  this._listeners = {};
  this._maxListeners = 10;
  this._joins = {};
  this._localKeys = {}; // key used as a foreign key by another model

  // This is to track joins that were not directly called by this model but that we still need
  // to purge the database
  this._reverseJoins = {};

  this._methods = {};
  this._staticMethods = {};
  this._async = {
    init: false,
    retrieve: false,
    save: false,
    validate: false
  };

  this._pre = {
    save: [],
    delete: [],
    validate: []
  };
  this._post = {
    init: [],
    retrieve: [],
    save: [],
    delete: [],
    validate: []
  };
}
```
- example usage
```shell
...
  util.loopKeys(self._getModel()._joins, function(joins, key) {
if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
  switch (joins[key].type) {
    case 'hasOne':
    case 'belongsTo':
      if (util.isPlainObject(self[key])) {
        if (self[key] instanceof Document === false) {
          self[key] = new self._getModel()._joins[key].model(self[key]);
        }
        // We do not propagate the options of this document, but only those given to validate
        var promise = self[key].validate(options, modelToValidate[key], validateAll, validatedModel, prefix+'['+key+']');
        if (promise instanceof Promise) {
          promises.push(promise);
          promise = null;
        }
...
```

#### <a name="apidoc.element.thinky.query"></a>[function <span class="apidocSignatureSpan">thinky.</span>query (model, query, options, error)](#apidoc.element.thinky.query)
- description and source-code
```javascript
function Query(model, query, options, error) {
  var self = this;

  this._model = model; // constructor of the model we should use for the results.
  if (model !== undefined) {
    this._r = model._getModel()._thinky.r;
    util.loopKeys(model._getModel()._staticMethods, function(staticMethods, key) {
      (function(_key) {
        self[_key] = function() {
          return staticMethods[_key].apply(self, arguments);
        };
      })(key);
    });
  }

  if (query !== undefined) {
    this._query = query;
   }
  else if (model !== undefined) {
    // By default, we initialize the query to 'r.table(<tableName>)'.
    this._query = this._r.table(model.getTableName());
  }

  if (util.isPlainObject(options)) {
    if (options.postValidation) {
      this._postValidation = options.postValidation === true;
    }
    if (options.ungroup) {
      this._ungroup = options.ungroup === true;
    }
    else {
      this._ungroup = false;
    }
  }
  else { // let the user rework the result after ungroup
    this._ungroup = false;
  }
  if (error) {
    // Note 'Query.prototype.error' is defined because of 'r.error', so we shouldn't
    // defined this.error.
    this._error = error;
  }
  this._pointWrite = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.document"></a>[module thinky.document](#apidoc.module.thinky.document)

#### <a name="apidoc.element.thinky.document.document"></a>[function <span class="apidocSignatureSpan">thinky.</span>document (model, options)](#apidoc.element.thinky.document.document)
- description and source-code
```javascript
function Document(model, options) {
  var self = this;  // Keep a reference to itself.

  this.constructor = model;  // The constructor for this model
  this._model = model._getModel(); // The instance of Model

  // We don't want to store options if they are different
  // than the one provided by the model
  if (util.isPlainObject(options)) {
    this._schemaOptions = {};
    this._schemaOptions.enforce_missing =
        (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
    this._schemaOptions.enforce_extra =
        (options.enforce_extra != null) ? options.enforce_extra : model.getOptions().enforce_extra;
    this._schemaOptions.enforce_type =
        (options.enforce_type != null) ? options.enforce_type : model.getOptions().enforce_type;
  }

  //TODO: We do not need to make a deep copy. We can do the same as for this._schemaOptions.
  options = options || {};
  this._options = {};
  this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : model.getOptions().timeFormat;
  this._options.validate = (options.validate != null) ? options.validate : model.getOptions().validate;

  this._saved = options.saved || false;  // Whether the document is saved or not

  util.bindEmitter(self);  // Copy methods from eventEmitter

  // links to hasOne/hasMany documents
  // We use it to know if some links have been removed/added before saving.
  // Example: { key: doc } or { key: [docs] }
  this._belongsTo = {};
  this._hasOne = {};
  this._hasMany = {};
  // Example: { <linkTableName>: { <valueOfRightKey>: true, ... }, ... }
  this._links = {}

  // Keep reference of any doc having a link pointing to this
  // So we can clean when users do doc.belongsToDoc.delete()
  this._parents = {
    _hasOne: {},      // <tableName>: [{doc, key}]
    _hasMany: {},     // <tableName>: [{doc, key}]
    _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
    _belongsLinks: {} // <tableName>: [{doc, key}]
  }

  // Bind listeners of the model to this documents.
  util.loopKeys(model._listeners, function(listeners, eventKey) {
    for(var j=0; j<listeners[eventKey].length; j++) {
      if (listeners[eventKey][j].once === false) {
        self.addListener(eventKey, listeners[eventKey][j].listener);
      }
      else if (listeners[eventKey][j].once === true) {
        self.once(eventKey, listeners[eventKey][j].listener);
      }
    }
  });


  // Atom feed
  this._active = false;
  this._feed = null;

  // Add customized methods of the model on this document.
  util.loopKeys(model._methods, function(methods, key) {
    if (self[key] === undefined) {
      self[key] = methods[key];
    }
    else {
      //TODO: Should we warn the users? Throw an error?
      console.log(self[key]);
      console.log("A property "+key+" is already defined in the prototype chain. Skipping.");
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.document.prototype"></a>[module thinky.document.prototype](#apidoc.module.thinky.document.prototype)

#### <a name="apidoc.element.thinky.document.prototype.__makeSavableCopy"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>__makeSavableCopy (doc, schema, options, model, r)](#apidoc.element.thinky.document.prototype.__makeSavableCopy)
- description and source-code
```javascript
__makeSavableCopy = function (doc, schema, options, model, r) {
  var localOptions; // can be undefined
  if (schema !== undefined) {
    localOptions = schema._options;
  }

  // model is an instance of a Model (for the top level fields), or undefined
  var result, key, keys, nextSchema, copyFlag;
  if (type.isDate(schema) && (typeof doc === 'string' || typeof doc === 'number')) {
    if (typeof doc === 'number') {
      var numericDate = parseInt(doc, 10);
      if(!isNaN(numericDate)) {
        doc = numericDate;
      }
    }
    return new Date(doc); // Use r.ISO8601 and not 'new Date()' to keep timezone
  }
  else if (type.isPoint(schema)) {
    if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
      var keys = Object.keys(doc).sort();
      if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (
typeof doc.longitude === "number")) {
        return r.point(doc.longitude, doc.latitude)
      }
      else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
        return r.geojson(doc)
      }
    }
    else if (Array.isArray(doc)) {
      if ((doc.length === 2) && (typeof doc[0] === "number") && (typeof doc[1] === "number")) {
        return r.point(doc[0], doc[1])
      }
    }
    else { // no transformation are required here, return doc
      return doc;
    }
  }
  else if (type.isNumber(schema) && (typeof doc === 'string')) {
    var numericString = parseFloat(doc);
    if(!isNaN(numericString)){
      return numericString;
    }else{
      return doc;
    }
  }

  if (util.isPlainObject(doc) && (doc instanceof Buffer === false)) {
    result = {};
    util.loopKeys(doc, function(doc, key) {
      copyFlag = true;
      if ((util.isPlainObject(model) === false) || (model._joins[key] === undefined)) { // We do not copy joined documents
        if ((schema !== undefined) && (schema._schema !== undefined) && (type.isVirtual(schema._schema[key]) === true)) {
          // We do not copy virtual
        }
        else if (((schema === undefined) || (schema._schema === undefined) || (schema._schema[key] === undefined)) &&
            (localOptions !== undefined) && (localOptions.enforce_extra === "remove")) {
          // We do not copy fields if enfroce_extra is "remove"
        }
        else {
          if ((schema !== undefined) && (schema._schema !== undefined)) {
            nextSchema = schema._schema[key];
          }
          else {
            nextSchema = undefined;
          }
          result[key] = Document.prototype.__makeSavableCopy(doc[key], nextSchema, localOptions, undefined, r);
        }
      }
    });

    // Copy the fields that are used as foreign keys
    if (util.isPlainObject(model) === true) {
      util.loopKeys(model._localKeys, function(localKeys, localKey) {
        if (doc[localKey] !== undefined) {
          if (schema !== undefined) {
            nextSchema = schema._schema[key];
          }
          else {
            nextSchema = undefined;
          }
          //TODO: Do we want to copy the foreign key value? If yes, there's no need for this loop
          //Do we want to copy the key from the joined document? If yes we need to replace doc[localKey]
          result[localKey] = Document.prototype.__makeSavableCopy(doc[localKey], nextSchema, localOptions, undefined, r);
        }
      });
    }
    return result;
  }
  else if (Array.isArray(doc)) {
    result = [];
    copyFlag = true;

    // Next schema
    if (type.isArray(schema)) {
      nextSchema = schema._schema;
    }
    else if ((util.isPlainObject(schema)) && (schema._type !== undefined) && (schema._schema !== undefined)) {
      nextSchema = schema._schema
      if (schema._type === "virtual") {
        copyFlag = false;
      }
    }
    else {
      nextSchema = undefined;
    }
    if (copyFlag === true) {
      for(var i=0; i<doc.length; i++) {
        result.push(Document.prototype.__makeSavableCopy(doc[i], nextSchema, localOptions, undefined, r));
      }
    }
    return result; ...
```
- example usage
```shell
...

 var r = this._getModel()._thinky.r;

 if (this._getModel().needToGenerateFields === true){
   this._generateDefault();
 }

 return this.__makeSavableCopy(this, schema, this._getOptions(), model, r)
}


/**
* Internal helper for _makeSavableCopy.
* generating the dfault and virtual fields.
* @return {any} the copy of the field/object.
...
```

#### <a name="apidoc.element.thinky.document.prototype._batchSave"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_batchSave (executeInsert)](#apidoc.element.thinky.document.prototype._batchSave)
- description and source-code
```javascript
_batchSave = function (executeInsert) {
  // Keep in sync with _save
  var self = this;
  self.emit('saving', self);

  return util.hook({
    preHooks: self._getModel()._pre.save,
    postHooks: self._getModel()._post.save,
    doc: self,
    async: true,
    fn: self._batchSaveSelf,
    fnArgs: [executeInsert]
  });
}
```
- example usage
```shell
...
  });
}

if (foundNonValidDoc === false) {
  Promise.all(promises).then(function() {
    var promises = [];
    for(var i=0; i<docs.length; i++) {
      promises.push(docs[i]._batchSave(executeInsert));
    }
    Promise.all(promises).then(function() {
      mainResolve(docs);
    }).error(function(error) {
      mainReject(error)
    });
  }).error(function(error) {
...
```

#### <a name="apidoc.element.thinky.document.prototype._batchSaveSelf"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_batchSaveSelf (executeInsert)](#apidoc.element.thinky.document.prototype._batchSaveSelf)
- description and source-code
```javascript
_batchSaveSelf = function (executeInsert) {
  var self = this;

  return new Promise(function(resolve, reject) {
    self.getModel().ready().then(function() {
      executeInsert(resolve, reject)
    });
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype._delete"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_delete (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback)](#apidoc.element.thinky.document.prototype._delete)
- description and source-code
```javascript
_delete = function (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback) {
  //TODO Set a (string) id per document and use it to perform faster lookup
  var self = this;

  if (util.isPlainObject(docToDelete) === false) {
    docToDelete = {};
  }

  deleteSelf = (deleteSelf === undefined) ? true: deleteSelf;

  return util.hook({
    preHooks: self._getModel()._pre.delete,
    postHooks: self._getModel()._post.delete,
    doc: self,
    async: true,
    fn: self._deleteHook,
    fnArgs: [docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback]
  });
}
```
- example usage
```shell
...
* removing the foreign key for hasOne/hasMany joined documents, and remove the
* links for hasAndBelongsToMany joined documents if the link is built on the
* primary key.
* @param {Function=} callback
* @return {Promise=} Return a promise if no callback is provided
*/
Document.prototype.delete = function(callback) {
 return this._delete({}, false, [], true, true, callback)
}


/**
* Delete the document from the database and the joined documents. If
* 'docToDelete' is undefined, it will delete all the joined documents, else it
* will limits itself to the one stored in the keys defined in 'docToDelete'.
...
```

#### <a name="apidoc.element.thinky.document.prototype._deleteHook"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_deleteHook (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback)](#apidoc.element.thinky.document.prototype._deleteHook)
- description and source-code
```javascript
_deleteHook = function (docToDelete, deleteAll, deletedDocs, deleteSelf, updateParents, callback) {
  var self = this;
  var model = self._getModel(); // instance of Model
  var constructor = self.getModel();
  var r = model._thinky.r;

  var promises = [];

  deletedDocs.push(self);
  util.loopKeys(self._getModel()._joins, function(joins, key) {
    if ((joins[key].type === 'hasOne') && (self[key] instanceof Document)) {
      if ((self[key].isSaved() === true) &&
        ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key]) === -1)))) {

        (function(key) {
          promises.push(new Promise(function(resolve, reject) {
            self[key]._delete(docToDelete[key], deleteAll, deletedDocs, true, false).then(function() {
              delete self[key];
              resolve();
            }).error(reject);
          }))
        })(key);
      }
      else if ((deleteSelf === true) && (deletedDocs.indexOf(self[key]) === -1)) {
        delete self[key][joins[key].rightKey];
        if (self[key].isSaved() === true) {
          promises.push(self[key].save({}, false, {}, true, false));
        }
      }
    }
    if ((joins[key].type === 'belongsTo') && (self[key] instanceof Document)) {
      if ((self[key].isSaved() === true) &&
        ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key]) === -1)))) {

        (function(key) {
          promises.push(new Promise(function(resolve, reject) {
            self[key]._delete(docToDelete[key], deleteAll, deletedDocs, true, false).then(function() {
              delete self[key];
              resolve();
            }).error(reject);
          }));
        })(key);
      }
    }

    if ((joins[key].type === 'hasMany') && (Array.isArray(self[key]))) {
      var manyPromises = [];
      for(var i=0; i<self[key].length; i++) {
        if (((self[key][i] instanceof Document) && (self[key][i].isSaved() === true))
          && ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key][i]) === -1)))) {

          manyPromises.push(self[key][i]._delete(docToDelete[key], deleteAll, deletedDocs, true, false))
        }
        else if ((self[key][i] instanceof Document) && (deletedDocs.indexOf(self[key][i]) === -1)) {
          delete self[key][i][joins[key].rightKey];
          if (self[key][i].isSaved() === true) {
            promises.push(self[key][i].save({}, false, {}, true, false))
          }
        }
      }
      (function(key) {
        promises.push(new Promise(function(resolve, reject) {
          Promise.all(manyPromises).then(function() {
            delete self[key];
            resolve()
          })
        }));
      })(key)
    }
    if ((joins[key].type === 'hasAndBelongsToMany') && (Array.isArray(self[key]))) {
      // Delete links + docs
      var pks = []; // primary keys of the documents
      var linksPks = []; // primary keys of the links

      // Store the element we are going to delete.
      // If the user force the deletion of the same element multiple times, we can't naively loop
      // over the elements in the array...
      var docsToDelete = [];


      for(var i=0; i<self[key].length; i++) {
        if (((self[key][i] instanceof Document) && (self[key][i].isSaved() === true))
          && ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key][i]) === -1)))) {

          //pks.push(self[key][i][joins[key].model._getModel()._pk]);
          docsToDelete.push(self[key][i]);
          // We are going to do a range delete, but we still have to recurse
          promises.push(self[key][i]._delete(docToDelete[key], deleteAll, deletedDocs, true, false))

          if (self.getModel()._getModel()._pk === joins[key].leftKey) {
            // The table is created since we are deleting an element from it
            if (self._getModel()._name === joins[key].model._getModel()._name) {
              if (self[joins[key].leftKey] < self[key][i][joins[key].rightKey]) {
                //TODO Add test for this
                linksPks.push(self[joins[key].leftKey]+"_"+s ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype._emitRetrieve"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_emitRetrieve ()](#apidoc.element.thinky.document.prototype._emitRetrieve)
- description and source-code
```javascript
_emitRetrieve = function () {
  var self = this;
  self.getModel().emit('retrieved', self);
  util.loopKeys(self._getModel()._joins, function(joins, key) {
    var join = joins[key];
    if ((joins[key].type === 'hasOne') || (joins[key].type === 'belongsTo')) {
      if ((self[key] != null) && (typeof self[key]._emitRetrieve === 'function')) {
        self[key]._emitRetrieve();
      }
    }
    else if ((joins[key].type === 'hasMany') || (joins[key].type === 'hasAndBelongsToMany')) {
      if (Array.isArray(self[key])) {
        for(var i=0; i<self[key].length; i++) {
          if (typeof self[key][i]._emitRetrieve === 'function') {
            self[key][i]._emitRetrieve();
          }
        }
      }
    }
  })
}
```
- example usage
```shell
...
Document.prototype._emitRetrieve = function() {
var self = this;
self.getModel().emit('retrieved', self);
util.loopKeys(self._getModel()._joins, function(joins, key) {
  var join = joins[key];
  if ((joins[key].type === 'hasOne') || (joins[key].type === 'belongsTo')) {
    if ((self[key] != null) && (typeof self[key]._emitRetrieve === 'function')) {
      self[key]._emitRetrieve();
    }
  }
  else if ((joins[key].type === 'hasMany') || (joins[key].type === 'hasAndBelongsToMany')) {
    if (Array.isArray(self[key])) {
      for(var i=0; i<self[key].length; i++) {
        if (typeof self[key][i]._emitRetrieve === 'function') {
          self[key][i]._emitRetrieve();
...
```

#### <a name="apidoc.element.thinky.document.prototype._generateDefault"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_generateDefault ()](#apidoc.element.thinky.document.prototype._generateDefault)
- description and source-code
```javascript
_generateDefault = function () {
  for(var i=0; i<this._getModel().defaultFields.length; i++) {
    schemaUtil.generateDefault(this, this._getModel().defaultFields[i], this);
  }
  if (this._getModel().virtualFields.length > 0) {
    this.generateVirtualValues();
  }
}
```
- example usage
```shell
...
Document.prototype._makeSavableCopy = function() {
  var model = this._getModel(); // instance of Model
  var schema = this._getModel()._schema;

  var r = this._getModel()._thinky.r;

  if (this._getModel().needToGenerateFields === true){
    this._generateDefault();
  }

  return this.__makeSavableCopy(this, schema, this._getOptions(), model, r)
}


/**
...
```

#### <a name="apidoc.element.thinky.document.prototype._getModel"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getModel ()](#apidoc.element.thinky.document.prototype._getModel)
- description and source-code
```javascript
_getModel = function () {
  return this.__proto__._model;
}
```
- example usage
```shell
...
 * @param {function} model The model of this document
 * @param {object=} options Options that can overwrite the ones of the model
 */
function Document(model, options) {
var self = this;  // Keep a reference to itself.

this.constructor = model;  // The constructor for this model
this._model = model._getModel(); // The instance of Model

// We don't want to store options if they are different
// than the one provided by the model
if (util.isPlainObject(options)) {
  this._schemaOptions = {};
  this._schemaOptions.enforce_missing =
      (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
...
```

#### <a name="apidoc.element.thinky.document.prototype._getOptions"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getOptions ()](#apidoc.element.thinky.document.prototype._getOptions)
- description and source-code
```javascript
_getOptions = function () {
  return this.__proto__._options;
}
```
- example usage
```shell
...

 var r = this._getModel()._thinky.r;

 if (this._getModel().needToGenerateFields === true){
   this._generateDefault();
 }

 return this.__makeSavableCopy(this, schema, this._getOptions(), model, r)
}


/**
* Internal helper for _makeSavableCopy.
* generating the dfault and virtual fields.
* @return {any} the copy of the field/object.
...
```

#### <a name="apidoc.element.thinky.document.prototype._getSchemaOptions"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getSchemaOptions ()](#apidoc.element.thinky.document.prototype._getSchemaOptions)
- description and source-code
```javascript
_getSchemaOptions = function () {
  return this.__proto__._schemaOptions;
}
```
- example usage
```shell
...
 * @return {Promise=} return a promise if the validation is asynchrone, else undefined.
 */
Document.prototype._validateHook = function(options, modelToValidate, validateAll, validatedModel, prefix) {
var self = this;
var promises = [];
var error;

var schemaOptions = self._getSchemaOptions();
if (util.isPlainObject(schemaOptions)) {
  schemaOptions = util.mergeOptions(schemaOptions, options);
}
else {
  schemaOptions = options;
}
...
```

#### <a name="apidoc.element.thinky.document.prototype._getVirtual"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_getVirtual ()](#apidoc.element.thinky.document.prototype._getVirtual)
- description and source-code
```javascript
_getVirtual = function () {
  return this.__proto__.virtualValue;
}
```
- example usage
```shell
...
/**
* Generate the virtual values for the document, or re-inject the ones
* previously saved.
* This should be called **after** '_generateDefault'.
*/
Document.prototype.generateVirtualValues = function() {
 for(var i=0; i<this._getModel().virtualFields.length; i++) {
   schemaUtil.generateVirtual(this, this._getModel().virtualFields[i], this, this._getVirtual());
 }
}


/**
* Generate the default values for the document, first the non virtual fields, and then
* the virtual fields.
...
```

#### <a name="apidoc.element.thinky.document.prototype._makeSavableCopy"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_makeSavableCopy ()](#apidoc.element.thinky.document.prototype._makeSavableCopy)
- description and source-code
```javascript
_makeSavableCopy = function () {
  var model = this._getModel(); // instance of Model
  var schema = this._getModel()._schema;

  var r = this._getModel()._thinky.r;

  if (this._getModel().needToGenerateFields === true){
    this._generateDefault();
  }

  return this.__makeSavableCopy(this, schema, this._getOptions(), model, r)
}
```
- example usage
```shell
...
// - Save this
// - Save hasOne, hasMany and hasAndBelongsToMany docs
// - Save links

// We'll use it to know which 'belongsTo' docs were saved
var belongsToKeysSaved = {};

var copy = self._makeSavableCopy();
self._saveVirtual();

// Save the joined documents via belongsTo first
var promises = [];
util.loopKeys(model._joins, function(joins, key) {
  if ((docToSave.hasOwnProperty(key) || (saveAll === true)) &&
      (joins[key].type === 'belongsTo') && ((saveAll === false) || (savedModel[joins[key].model.getTableName()] !== true))) {
...
```

#### <a name="apidoc.element.thinky.document.prototype._merge"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_merge (obj)](#apidoc.element.thinky.document.prototype._merge)
- description and source-code
```javascript
_merge = function (obj) {
  var self = this;
  util.loopKeys(self, function(self, key) {
    if ((obj[key] === undefined) && (self._getModel()._joins[key] === undefined)) {
      delete self[key];
    }
  });
  util.loopKeys(obj, function(obj, key) {
    self[key] = obj[key];
  });
  return self;
}
```
- example usage
```shell
...

  if (result.first_error != null) {
return reject(Errors.create(result.first_error));
  }

  util.tryCatch(function() { // Validate the doc, replace it, and tag it as saved
if (Array.isArray(result.changes) && result.changes.length > 0) {
  self._merge(result.changes[0].new_val);
  self._setOldValue(util.deepCopy(result.changes[0].old_val));
}

if (self._getModel().needToGenerateFields === true) {
  self._generateDefault();
}
self.setSaved();
...
```

#### <a name="apidoc.element.thinky.document.prototype._onSaved"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_onSaved (result, docToSave, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._onSaved)
- description and source-code
```javascript
_onSaved = function (result, docToSave, saveAll, savedModel, resolve, reject) {
  // Keep in sync with Model.save
  var self = this;

  if (result.first_error != null) {
    return reject(Errors.create(result.first_error));
  }

  util.tryCatch(function() { // Validate the doc, replace it, and tag it as saved
    if (Array.isArray(result.changes) && result.changes.length > 0) {
      self._merge(result.changes[0].new_val);
      self._setOldValue(util.deepCopy(result.changes[0].old_val));
    }

    if (self._getModel().needToGenerateFields === true) {
      self._generateDefault();
    }
    self.setSaved();
    self.emit('saved', self);

    var promise = self.validate();
    if (promise instanceof Promise) {
      promise.then(function() {
        self._saveMany(docToSave, saveAll, savedModel, resolve, reject)
      }).error(reject);
    }
    else {
      self._saveMany(docToSave, saveAll, savedModel, resolve, reject)
    }
  }, reject);
}
```
- example usage
```shell
...
    util.tryCatch(function() {
// Validate the document before saving it
var promise = self.validate();
if (promise instanceof Promise) {
  promise.then(function() {
    querySaveSelf = buildQuery();
    querySaveSelf.run().then(function(result) {
      self._onSaved(result, docToSave, saveAll, savedModel, resolve, reject)
    }).error(reject)
  }).error(reject);
}
else {
  querySaveSelf = buildQuery();
  querySaveSelf.run().then(function(result) {
    self._onSaved(result, docToSave, saveAll, savedModel, resolve, reject)
...
```

#### <a name="apidoc.element.thinky.document.prototype._onSavedBelongsTo"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_onSavedBelongsTo ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._onSavedBelongsTo)
- description and source-code
```javascript
_onSavedBelongsTo = function ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject) {
  var self = this;
  var model = self._getModel();
  var constructor = self.__proto__.constructor;
  var r = this._getModel()._thinky.r;

  util.loopKeys(belongsToKeysSaved, function(joins, key) {
    var joins = model._joins;
    if (self[key] != null) {

      self.__proto__._belongsTo[key] = true;

      // Copy foreign key
      if (self[key][joins[key].rightKey] == null) {
        if (self.hasOwnProperty(joins[key].leftKey)) {
          delete self[joins[key][joins[key].leftKey]];
        }
        if (copy.hasOwnProperty(joins[key].leftKey)) {
          delete copy[joins[key][joins[key].leftKey]];
        }
      }
      else {
        self[joins[key].leftKey] = self[key][joins[key].rightKey];
        copy[joins[key].leftKey] = self[key][joins[key].rightKey]; // We need to put it in copy before saving it
      }

      // Save the document that belongs to self[key]
      if (self[key].__proto__._parents._belongsTo[constructor.getTableName()] == null) {
        self[key].__proto__._parents._belongsTo[constructor.getTableName()] = [];
      }
      self[key].__proto__._parents._belongsTo[constructor.getTableName()].push({
        doc: self,
        foreignKey: joins[key].leftKey,
        key: key // foreignDoc
      });
    }
  });
  self._saveSelf(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)
}
```
- example usage
```shell
...
        }
      }
    });

    //TODO Remove once
    self.getModel().ready().then(function() {
      Promise.all(promises).then(function() {
        self._onSavedBelongsTo(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject);
      }).error(reject);
    });
  });
  return p;
}
...
```

#### <a name="apidoc.element.thinky.document.prototype._save"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_save (docToSave, saveAll, savedModel, callback)](#apidoc.element.thinky.document.prototype._save)
- description and source-code
```javascript
_save = function (docToSave, saveAll, savedModel, callback) {
  //TOIMPROVE? How should we handle circular references outsides of joined fields? Now we throw with a maximum call stack size exceed
  var self = this;
  self.emit('saving', self);

  return util.hook({
    preHooks: self._getModel()._pre.save,
    postHooks: self._getModel()._post.save,
    doc: self,
    async: true,
    fn: self._saveHook,
    fnArgs: [docToSave, saveAll, savedModel]
  }).nodeify(callback);
}
```
- example usage
```shell
...
/**
* Save the document and execute the hooks. Return a promise if the callback
* is not provided.
* @param {function=} callback to execute
* @return {Promise=}
*/
Document.prototype.save = function(callback) {
 return this._save({}, false, {}, callback);
}


/**
* Save the document and its joined documents. It will also execute the hooks.
* Return a promise if the callback is not provided.
* It will save joined documents as long as a document of the same model has not
...
```

#### <a name="apidoc.element.thinky.document.prototype._saveHook"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveHook (docToSave, saveAll, savedModel)](#apidoc.element.thinky.document.prototype._saveHook)
- description and source-code
```javascript
_saveHook = function (docToSave, saveAll, savedModel) {
  var self = this;
  var model = self._getModel(); // instance of Model
  var constructor = self.getModel();
  var r = model._thinky.r;

  if (util.isPlainObject(docToSave) === false) {
    docToSave = {};
  }

  savedModel[constructor.getTableName()] = true;


  var p = new Promise(function(resolve, reject) {
    // Steps:
    // - Save belongsTo
    // - Save this
    // - Save hasOne, hasMany and hasAndBelongsToMany docs
    // - Save links

    // We'll use it to know which 'belongsTo' docs were saved
    var belongsToKeysSaved = {};

    var copy = self._makeSavableCopy();
    self._saveVirtual();

    // Save the joined documents via belongsTo first
    var promises = [];
    util.loopKeys(model._joins, function(joins, key) {
      if ((docToSave.hasOwnProperty(key) || (saveAll === true)) &&
          (joins[key].type === 'belongsTo') && ((saveAll === false) || (savedModel[joins[key].model.getTableName()] !== true))) {

        belongsToKeysSaved[key] = true;
        if (self[key] != null) {
          savedModel[joins[key].model.getTableName()] = true;
          if (saveAll === true) {
            promises.push(self[key]._save({}, true, savedModel))
          }
          else {
            promises.push(self[key]._save(docToSave[joins[key].model.getTableName()], false, savedModel))
          }
        }
      }
    });

    //TODO Remove once
    self.getModel().ready().then(function() {
      Promise.all(promises).then(function() {
        self._onSavedBelongsTo(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject);
      }).error(reject);
    });
  });
  return p;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype._saveLinks"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveLinks (docToSave, saveAll, resolve, reject)](#apidoc.element.thinky.document.prototype._saveLinks)
- description and source-code
```javascript
_saveLinks = function (docToSave, saveAll, resolve, reject) {
  var self = this;
  var model = self._getModel();
  var constructor = self.getModel();
  var r = model._thinky.r;

  var promisesLink = [];

  util.loopKeys(model._joins, function(joins, key) {
    // Write tests about that!
    if (((key in docToSave) || (saveAll === true)) &&
        (joins[key].type === 'hasAndBelongsToMany')) {

      if (Array.isArray(self[key])) {
        var newKeys = {}
        for(var i=0; i<self[key].length; i++) {
          if (util.isPlainObject(self[key][i])) {
            if (self[key][i].isSaved() === true) {
              newKeys[self[key][i][joins[key].rightKey]] = true;
            }
          }
          else { // self[key][i] is just the key
            newKeys[self[key][i]] = true;
          }
        }

        if (self.__proto__._links[joins[key].link] === undefined) {
          self.__proto__._links[joins[key].link] = {}
        }
        var oldKeys = self.__proto__._links[joins[key].link];

        util.loopKeys(newKeys, function(newKeys, link) {
          if (oldKeys[link] !== true) {
            var newLink = {};

            if ((constructor.getTableName() === joins[key].model.getTableName())
              && (joins[key].leftKey === joins[key].rightKey)) {

              // We link on the same model and same key
              // We don't want to save redundant field
              if (link < self[joins[key].leftKey]) {
                newLink.id = link+"_"+self[joins[key].leftKey];
              }
              else {
                newLink.id = self[joins[key].leftKey]+"_"+link;
              }
              newLink[joins[key].leftKey+"_"+joins[key].leftKey] = [link, self[joins[key].leftKey]];
            }
            else {
              newLink[constructor.getTableName()+"_"+joins[key].leftKey] = self[joins[key].leftKey];
              newLink[joins[key].model.getTableName()+"_"+joins[key].rightKey] = link;

              // Create the primary key
              if (constructor.getTableName() < joins[key].model.getTableName()) {
                newLink.id = self[joins[key].leftKey]+"_"+link;
              }
              else if (constructor.getTableName() > joins[key].model.getTableName()) {
                newLink.id = link+"_"+self[joins[key].leftKey];
              }
              else {
                if (link < self[joins[key].leftKey]) {
                  newLink.id = link+"_"+self[joins[key].leftKey];
                }
                else {
                  newLink.id = self[joins[key].leftKey]+"_"+link;
                }
              }
            }

            (function(key, link) {
              promisesLink.push(new Promise(function(resolve, reject) {
                r.table(self._getModel()._joins[key].link).insert(newLink, {conflict: "replace", returnChanges: 'always'}).run().
then(function(result) {
                  if (Array.isArray(result.changes) && result.changes.length > 0) {
                    self.__proto__._links[joins[key].link][result.changes[0].new_val[joins[key].model.getTableName()+"_"+joins[key
].rightKey]] = true;
                  }
                  else {
                    self.__proto__._links[joins[key].link][newLink[joins[key].model.getTableName()+"_"+joins[key].rightKey]] = true
;
                  }
                  resolve();
                }).error(reject);
              }))
            })(key, link);
          }
        });

        var keysToDelete = []
        util.loopKeys(oldKeys, function(oldKeys, link) {
          if (newKeys[link] === undefined) {
            if (constructor.getTableName() < joins[key].model.getTableName()) {
              keysToDelete.push(self[joins[key].leftKey]+"_"+link);
            }
            else {
              keysToDelete.push(link+"_"+self[joins[key].leftKey]);
            }
          }
        });
        if (keysToDelete.length > 0) {
          var table = r.table(joins[key].link);
          promisesLink.push(table.getAll.apply(table, keysToDelete).delete().run().then(function() {
            for(var i=0; i<keysToDelete.length; i++) ...
```
- example usage
```shell
...
        }
      }
    }
  });

  if (promisesMany.length > 0) {
    Promise.all(promisesMany).then(function() {
      self._saveLinks(docToSave, saveAll, resolve, reject)
    }).error(reject);
  }
  else {
    self._saveLinks(docToSave, saveAll, resolve, reject)
  }
}
...
```

#### <a name="apidoc.element.thinky.document.prototype._saveMany"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveMany (docToSave, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._saveMany)
- description and source-code
```javascript
_saveMany = function (docToSave, saveAll, savedModel, resolve, reject) {
  var self = this;
  var model = self._getModel();

  var promisesMany = [];
  util.loopKeys(model._joins, function(joins, key) {
    if (((key in docToSave) || (saveAll === true)) &&
        (joins[key].type === 'hasOne') && ((saveAll === false) || (savedModel[joins[key].model.getTableName()] !== true))) {
      savedModel[joins[key].model.getTableName()] = true;

      if (self[key] != null) {
        self[key][joins[key].rightKey] = self[joins[key].leftKey];
        (function(_key) {
          promisesMany.push(new Promise(function(resolve, reject) {
            self[_key]._save(docToSave[_key], saveAll, savedModel).then(function() {
              self.__proto__._hasOne[_key] = {
                doc: self[_key],
                foreignKey: self._getModel()._joins[_key].rightKey
              };
              if (self[_key].__proto__._parents._hasOne[self._getModel()._name] == null) {
                self[_key].__proto__._parents._hasOne[self._getModel()._name] = [];
              }
              self[_key].__proto__._parents._hasOne[self._getModel()._name].push({
                doc: self,
                key: key
              });
              resolve();
            }).error(reject);
          }))
        })(key)
      }
      else if ((self[key] == null) && (self.__proto__._hasOne[key] != null)) {
        var doc = self.__proto__._hasOne[key].doc;
        delete doc[self.__proto__._hasOne[key].foreignKey];
        promisesMany.push(doc._save(docToSave[key], saveAll, savedModel))
        self.__proto__._hasOne[key] = null;
      }
    }
  });
  util.loopKeys(model._joins, function(joins, key) {
    if (((key in docToSave) || (saveAll === true)) &&
        (joins[key].type === 'hasMany') && ((saveAll === false) || (savedModel[joins[key].model.getTableName()] !== true))
        && (Array.isArray(self[key]))) {

      savedModel[joins[key].model.getTableName()] = true;

      //Go through _hasMany and find element that were removed
      var pkMap = {};
      if (Array.isArray(self[key])) {
        for(var i=0; i<self[key].length; i++) {
          if (self[key][i][joins[key].model._pk] != null) {
            pkMap[self[key][i][joins[key].model._pk]] = true;
          }
        }
      }

      if (self.__proto__._hasMany[key] != null) {
        for(var i=0; i<self.__proto__._hasMany[key].length; i++) {
          if (pkMap[self.__proto__._hasMany[key][i].doc[[joins[key].model._pk]]] == null) {
            delete self.__proto__._hasMany[key][i].doc[self.__proto__._hasMany[key][i].foreignKey];
            promisesMany.push(self.__proto__._hasMany[key][i].doc._save(docToSave[key], saveAll, savedModel));
          }
        }
      }
      self.__proto__._hasMany[key] = [];

      for(var i=0; i<self[key].length; i++) {
        self[key][i][joins[key].rightKey] = self[joins[key].leftKey];
        (function(key, i) {
          promisesMany.push(new Promise(function(resolve, reject) {
            if (!(self[key][i] instanceof Document)) {
              self[key][i] = new joins[key].model(self[key][i]);
            }

            var callback = function() {
              self[key][i]._save(docToSave[key], saveAll, savedModel).then(function(doc) {
                if (!Array.isArray(self.__proto__._hasMany[key])) {
                  self.__proto__._hasMany[key] = [];
                }
                self.__proto__._hasMany[key].push({
                  doc: doc,
                  foreignKey: self._getModel()._joins[key].rightKey
                });

                if (self[key][i].__proto__._parents._hasMany[self._getModel()._name] == null) {
                  self[key][i].__proto__._parents._hasMany[self._getModel()._name] = [];
                }
                self[key][i].__proto__._parents._hasMany[self._getModel()._name].push({
                  doc: self,
                  key: key
                });

                resolve();
              }).error(reject);
            }

            if (self[key][i] instanceof Promise) {
              self[key][i].then(cal ...
```
- example usage
```shell
...
    }
    self.setSaved();
    self.emit('saved', self);

    var promise = self.validate();
    if (promise instanceof Promise) {
      promise.then(function() {
        self._saveMany(docToSave, saveAll, savedModel, resolve, reject)
      }).error(reject);
    }
    else {
      self._saveMany(docToSave, saveAll, savedModel, resolve, reject)
    }
  }, reject);
}
...
```

#### <a name="apidoc.element.thinky.document.prototype._saveSelf"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveSelf ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)](#apidoc.element.thinky.document.prototype._saveSelf)
- description and source-code
```javascript
_saveSelf = function ( copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject) {
  var self = this;
  var model = self._getModel();
  var constructor = self.__proto__.constructor;
  var r = this._getModel()._thinky.r;

  // BelongsTo documents were saved before. We just need to copy the foreign
  // keys.
  util.loopKeys(model._joins, function(joins, key) {
    if ((joins[key].type === 'belongsTo') && (belongsToKeysSaved[key] === true)) {
      if (self[key] != null) {
        self[joins[key].leftKey] = self[key][joins[key].rightKey]
      }
      else if (self.__proto__._belongsTo[key]) {
        delete self[joins[key].leftKey];
        delete copy[joins[key].leftKey];
      }
    }
  });

  var querySaveSelf; // The query to save the document on which 'save'/'saveAll' was called.
  // We haven't validated the document yet, so building the query with 'copy'
  // may throw an error (for example if a Date has not a valid time).
  var buildQuery = function () {
    if (self.__proto__._saved === false) {
      return querySaveSelf = r.table(constructor.getTableName())
        .insert(copy, {returnChanges: 'always'})
    }
    else {
      if (copy[model._pk] === undefined) {
        throw new Error("The document was previously saved, but its primary key is undefined.");
      }
      return querySaveSelf = r.table(constructor.getTableName())
        .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
    }
  }

  self.getModel().ready().then(function() {
    util.tryCatch(function() {
      // Validate the document before saving it
      var promise = self.validate();
      if (promise instanceof Promise) {
        promise.then(function() {
          querySaveSelf = buildQuery();
          querySaveSelf.run().then(function(result) {
            self._onSaved(result, docToSave, saveAll, savedModel, resolve, reject)
          }).error(reject)
        }).error(reject);
      }
      else {
        querySaveSelf = buildQuery();
        querySaveSelf.run().then(function(result) {
          self._onSaved(result, docToSave, saveAll, savedModel, resolve, reject)
        }).error(reject)
      }
    }, reject);
  });
}
```
- example usage
```shell
...
     self[key].__proto__._parents._belongsTo[constructor.getTableName()].push({
       doc: self,
       foreignKey: joins[key].leftKey,
       key: key // foreignDoc
     });
   }
 });
 self._saveSelf(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject)
}


/**
* Save the document on which 'save' was called.
* @param {!Object} copy The savable copy of the original documents.
* @param {Object=} docToSave Documents to save represented by an object field->true
...
```

#### <a name="apidoc.element.thinky.document.prototype._saveVirtual"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_saveVirtual ()](#apidoc.element.thinky.document.prototype._saveVirtual)
- description and source-code
```javascript
_saveVirtual = function () {
  var copy = {};
  var model = this._getModel(); // instance of Model

  // TODO We could do better and copy less things, but things get a bit tricky
  // when virtual fields are nested in arrays.
  // This implementation still allows no overhead if no virtual fields exist,
  // which should be the most common case
  for(var i=0; i<this._getModel().virtualFields.length; i++) {
    var key = this._getModel().virtualFields[i].path[0];
    copy[key] = this[key];
  }
  this.__proto__.virtualValue = util.deepCopy(copy);
}
```
- example usage
```shell
...
// - Save hasOne, hasMany and hasAndBelongsToMany docs
// - Save links

// We'll use it to know which 'belongsTo' docs were saved
var belongsToKeysSaved = {};

var copy = self._makeSavableCopy();
self._saveVirtual();

// Save the joined documents via belongsTo first
var promises = [];
util.loopKeys(model._joins, function(joins, key) {
  if ((docToSave.hasOwnProperty(key) || (saveAll === true)) &&
      (joins[key].type === 'belongsTo') && ((saveAll === false) || (savedModel[joins[key].model.getTableName()] !== true))) {
...
```

#### <a name="apidoc.element.thinky.document.prototype._setFeed"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setFeed (feed)](#apidoc.element.thinky.document.prototype._setFeed)
- description and source-code
```javascript
_setFeed = function (feed) {
  var self = this;

  self.__proto__._feed = feed;
  self.__proto__._active = true;
  feed.each(function(err, change) {
    if (err) {
      self.__proto__._active = false;
      self.emit('error', err);
    }
    else {
      if (change.new_val === null) {
        // Delete all the fields
        self._merge({});
        self._setOldValue(change.old_val);
        self._setUnSaved();
        self.emit('change', self);
      }
      else {
        self._merge(change.new_val);
        self._setOldValue(change.old_val);
        self.setSaved();
        self.emit('change', self);
      }
    }

  });
}
```
- example usage
```shell
...
    return feed;
  }

  if (resultType === 'AtomFeed') {
    return result.next().then(function(initial) {
      var value = initial.new_val || {};
      return self._model._parse(value).then(function(doc) {
        doc._setFeed(result);
        return doc;
      });
    });
  }
}

if (parse === true) {
...
```

#### <a name="apidoc.element.thinky.document.prototype._setOldValue"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setOldValue (value)](#apidoc.element.thinky.document.prototype._setOldValue)
- description and source-code
```javascript
_setOldValue = function (value) {
  return this.__proto__.oldValue = value;
}
```
- example usage
```shell
...
  if (result.first_error != null) {
return reject(Errors.create(result.first_error));
  }

  util.tryCatch(function() { // Validate the doc, replace it, and tag it as saved
if (Array.isArray(result.changes) && result.changes.length > 0) {
  self._merge(result.changes[0].new_val);
  self._setOldValue(util.deepCopy(result.changes[0].old_val));
}

if (self._getModel().needToGenerateFields === true) {
  self._generateDefault();
}
self.setSaved();
self.emit('saved', self);
...
```

#### <a name="apidoc.element.thinky.document.prototype._setUnSaved"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_setUnSaved ()](#apidoc.element.thinky.document.prototype._setUnSaved)
- description and source-code
```javascript
_setUnSaved = function () {
  this.__proto__._saved = false;
}
```
- example usage
```shell
...
  });
}

if (deleteSelf !== false) {
  if (self.isSaved() === true) {
    promises.push(new Promise(function(resolve, reject) {
      r.table(model._name).get(self[model._pk]).delete().run().then(function(result) {
        self._setUnSaved();
        self.emit('deleted', self);
        resolve(self);
      }).error(reject);
    }))
  }
  // else we don't throw an error, should we?
}
...
```

#### <a name="apidoc.element.thinky.document.prototype._validateHook"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_validateHook (options, modelToValidate, validateAll, validatedModel, prefix)](#apidoc.element.thinky.document.prototype._validateHook)
- description and source-code
```javascript
_validateHook = function (options, modelToValidate, validateAll, validatedModel, prefix) {
  var self = this;
  var promises = [];
  var error;

  var schemaOptions = self._getSchemaOptions();
  if (util.isPlainObject(schemaOptions)) {
    schemaOptions = util.mergeOptions(schemaOptions, options);
  }
  else {
    schemaOptions = options;
  }


  if (typeof self._getModel()._validator === 'function') {
    if (self._getModel()._validator.call(self, self) === false) {
      throw new Errors.ValidationError("Document's validator returned 'false'.");
    }
  }

  // Validate this document
  self._getModel()._schema.validate(self, prefix, schemaOptions)

  if (util.isPlainObject(modelToValidate) === false) {
    modelToValidate = {};
  }

  var constructor = self.__proto__.constructor;
  validatedModel[constructor.getTableName()] = true;

  // Validate joined documents
  util.loopKeys(self._getModel()._joins, function(joins, key) {
    if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          if (util.isPlainObject(self[key])) {
            if (self[key] instanceof Document === false) {
              self[key] = new self._getModel()._joins[key].model(self[key]);
            }
            // We do not propagate the options of this document, but only those given to validate
            var promise = self[key].validate(options, modelToValidate[key], validateAll, validatedModel, prefix+'['+key+']');
            if (promise instanceof Promise) {
              promises.push(promise);
              promise = null;
            }
          }
          else if (self[key] != null) {
            throw new Errors.ValidationError("Joined field "+prefix+"["+key+"] should be 'undefined', 'null' or an 'Object'")
          }
          break;

        case 'hasMany':
        case 'hasAndBelongsToMany':
          if (Array.isArray(self[key])) {
            for(var i=0; i<self[key].length; i++) {
              if (util.isPlainObject(self[key][i])) {
                if (self[key][i] instanceof Document === false) {
                  self[key][i] = new self._getModel()._joins[key].model(self[key][i]);
                }
                promise = self[key][i].validate(options, modelToValidate[key], validateAll, validatedModel, prefix+'['+key+']['+
i+']');
                if (promise instanceof Promise) {
                  promises.push(promise);
                  promise = null;
                }
              }
              else {
                throw new Errors.ValidationError("Joined field "+prefix+"["+key+"]["+i+"] should be 'undefined', 'null' or an 'Array
'")
              }
            }
          }
          else if (self[key] != null) {
            throw new Errors.ValidationError("Joined field "+prefix+"["+key+"] should be 'undefined', 'null' or an 'Array'")
          }
          break;
      }
    }
  });
  if (promises.length > 0) {
    return Promise.all(promises);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype._validateIsAsync"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>_validateIsAsync (modelToValidate, validateAll, validatedModel)](#apidoc.element.thinky.document.prototype._validateIsAsync)
- description and source-code
```javascript
_validateIsAsync = function (modelToValidate, validateAll, validatedModel) {
  var self = this;

  if (self._getModel()._async.validate) {
    return true;
  }
  var async = false;
  util.loopKeys(self._getModel()._joins, function(joins, key) {
    if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
      if (((joins[key].type === 'hasOne') || (joins[key].type === 'belongsTo'))) {
        if (util.isPlainObject(self[key])) {
          if (self[key] instanceof Document === false) {
            self[key] = new self._getModel()._joins[key].model(self[key]);
          }
          // We do not propagate the options of this document, but only those given to validate
          if (self[key]._getModel()._async.validate || self[key]._validateIsAsync(modelToValidate, validateAll, validatedModel)) {
            async = true;
            return false;
          }
        }
      }
      else  if (((joins[key].type === 'hasMany') || (joins[key].type === 'hasAndBelongsToMany'))) {
        if (Array.isArray(self[key])) {
          for(var i=0; i<self[key].length; i++) {
            if (util.isPlainObject(self[key][i])) {
              if (self[key][i] instanceof Document === false) {
                self[key][i] = new self._getModel()._joins[key].model(self[key][i]);
              }
              if (self[key][i]._getModel()._async.validate || self[key][i]._validateIsAsync(modelToValidate, validateAll, validatedModel
)) {
                async = true;
                return false;
              }
            }
          }
        }
      }
    }
    return false;
  });
  return async;
}
```
- example usage
```shell
...
validatedModel = validatedModel || {};
prefix = prefix || '';

var self = this;
var validatedModelCopy = util.deepCopy(validatedModel);

//TODO: Can we not always call this?
var async = self._validateIsAsync(modelToValidate, validateAll, validatedModelCopy);

return util.hook({
  preHooks: self._getModel()._pre.validate,
  postHooks: self._getModel()._post.validate,
  doc: self,
  async: async,
  fn: self._validateHook,
...
```

#### <a name="apidoc.element.thinky.document.prototype.addRelation"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>addRelation ()](#apidoc.element.thinky.document.prototype.addRelation)
- description and source-code
```javascript
addRelation = function () {
  var self = this;
  var pk = self._getModel()._pk;

  var query = self.getModel().get(this[pk])
  return query.addRelation.apply(query, arguments);
}
```
- example usage
```shell
...
/**
* Add a relation
* @param {string} field The field of the joined document(s)
* @param {Object} joinedDocument An object with the primary key defined or the related key
* @return {Promise}
*
* hasOne, primary key required
* User.get(1).addRelation("account", {id: 2, sold: 2132})
* The promise resolved the document on which addRelation is called
*
* hasMany, primary key required
* User.get(1).addRelation("accounts", {id: 2, sold: 2132})
* The promise resolved the updated joined document
*
* belongsTo, right joined key OR primary key required
...
```

#### <a name="apidoc.element.thinky.document.prototype.closeFeed"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>closeFeed ()](#apidoc.element.thinky.document.prototype.closeFeed)
- description and source-code
```javascript
closeFeed = function () {
  return this.__proto__._feed.close();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.delete"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>delete (callback)](#apidoc.element.thinky.document.prototype.delete)
- description and source-code
```javascript
delete = function (callback) {
  return this._delete({}, false, [], true, true, callback)
}
```
- example usage
```shell
...
this._belongsTo = {};
this._hasOne = {};
this._hasMany = {};
// Example: { <linkTableName>: { <valueOfRightKey>: true, ... }, ... }
this._links = {}

// Keep reference of any doc having a link pointing to this
// So we can clean when users do doc.belongsToDoc.delete()
this._parents = {
  _hasOne: {},      // <tableName>: [{doc, key}]
  _hasMany: {},     // <tableName>: [{doc, key}]
  _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
  _belongsLinks: {} // <tableName>: [{doc, key}]
}
...
```

#### <a name="apidoc.element.thinky.document.prototype.deleteAll"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>deleteAll (docToDelete, callback)](#apidoc.element.thinky.document.prototype.deleteAll)
- description and source-code
```javascript
deleteAll = function (docToDelete, callback) {
  var deleteAll;
  if (typeof docToDelete === 'function') {
    callback = docToDelete;
    deleteAll = true;
    docToDelete = {};
  }
  else {
    deleteAll = docToDelete === undefined;
    docToDelete = docToDelete || {};
  }
  return this._delete(docToDelete, deleteAll, [], true, true, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.generateVirtualValues"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>generateVirtualValues ()](#apidoc.element.thinky.document.prototype.generateVirtualValues)
- description and source-code
```javascript
generateVirtualValues = function () {
  for(var i=0; i<this._getModel().virtualFields.length; i++) {
    schemaUtil.generateVirtual(this, this._getModel().virtualFields[i], this, this._getVirtual());
  }
}
```
- example usage
```shell
...
* the virtual fields.
*/
Document.prototype._generateDefault = function() {
 for(var i=0; i<this._getModel().defaultFields.length; i++) {
   schemaUtil.generateDefault(this, this._getModel().defaultFields[i], this);
 }
 if (this._getModel().virtualFields.length > 0) {
   this.generateVirtualValues();
 }
}


/*
* Validate this document against the schema of its model and triggers all the hooks.
* @param {Object=} options Options to overwrite the ones of the document.
...
```

#### <a name="apidoc.element.thinky.document.prototype.getFeed"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getFeed ()](#apidoc.element.thinky.document.prototype.getFeed)
- description and source-code
```javascript
getFeed = function () {
  return this.__proto__._feed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.getModel"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getModel ()](#apidoc.element.thinky.document.prototype.getModel)
- description and source-code
```javascript
getModel = function () {
  return this.__proto__.constructor;
}
```
- example usage
```shell
...
 * @param {Function} executeInsert the method that will execute the batch insert
 * @return {Promise}
 */
Document.prototype._batchSaveSelf = function(executeInsert) {
  var self = this;

  return new Promise(function(resolve, reject) {
    self.getModel().ready().then(function() {
      executeInsert(resolve, reject)
    });
  })
}


/**
...
```

#### <a name="apidoc.element.thinky.document.prototype.getOldValue"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>getOldValue ()](#apidoc.element.thinky.document.prototype.getOldValue)
- description and source-code
```javascript
getOldValue = function () {
  return this.__proto__.oldValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.isSaved"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>isSaved ()](#apidoc.element.thinky.document.prototype.isSaved)
- description and source-code
```javascript
isSaved = function () {
  return this.__proto__._saved;
}
```
- example usage
```shell
...
    if (((key in docToSave) || (saveAll === true)) &&
  (joins[key].type === 'hasAndBelongsToMany')) {

if (Array.isArray(self[key])) {
  var newKeys = {}
  for(var i=0; i<self[key].length; i++) {
    if (util.isPlainObject(self[key][i])) {
      if (self[key][i].isSaved() === true) {
        newKeys[self[key][i][joins[key].rightKey]] = true;
      }
    }
    else { // self[key][i] is just the key
      newKeys[self[key][i]] = true;
    }
  }
...
```

#### <a name="apidoc.element.thinky.document.prototype.merge"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>merge (obj)](#apidoc.element.thinky.document.prototype.merge)
- description and source-code
```javascript
merge = function (obj) {
  var self = this;
  util.loopKeys(obj, function(obj, key) {
    // Recursively merge only if both fields are objects, else we'll overwrite the field
    if (util.isPlainObject(obj[key]) && util.isPlainObject(self[key])) {
      Document.prototype.merge.call(self[key], obj[key])
    }
    else {
      self[key] = obj[key];
    }
  });
  return self;
}
```
- example usage
```shell
...
  gotModel[model.getTableName()] = true;

  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
...
```

#### <a name="apidoc.element.thinky.document.prototype.purge"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>purge (callback)](#apidoc.element.thinky.document.prototype.purge)
- description and source-code
```javascript
purge = function (callback) {
  var self = this;

  var model = self._getModel(); // instance of Model
  var r = model._thinky.r;

  // Clean parent for hasOne
  // doc.otherDoc.delete()
  util.loopKeys(self.__proto__._parents._hasOne, function(hasOne, key) {
    for(var i=0; i<hasOne[key].length; i++) {
      var parentDoc = hasOne[key][i].doc; // A doc that belongs to otherDoc (aka this)
      delete parentDoc[hasOne[key][i].key] // Delete reference to otherDoc (aka this)
    }
  });

  // Clean parent for belongsTo
  // doc.otherDoc.delete()
  util.loopKeys(self.__proto__._parents._belongsTo, function(belongsTo, key) {
    for(var i=0; i<belongsTo[key].length; i++) {
      var parentDoc = belongsTo[key][i].doc;
      delete parentDoc[belongsTo[key][i].key];
      delete parentDoc[belongsTo[key][i].foreignKey];
    }
  });

  // Clean parent for hasMany
  util.loopKeys(self.__proto__._parents._hasMany, function(hasMany, key) {
    for(var i=0; i<hasMany[key].length; i++) {
      var parentDoc = hasMany[key][i].doc;
      var field = hasMany[key][i].key;
      for(var j=0; j<parentDoc[field].length; j++) {
        if (parentDoc[field][j] === this) {
          parentDoc[field].splice(j, 1);
          break;
        }
      }
    }
  });


  // Clean parent for hasAndBelongsToMany
  util.loopKeys(self.__proto__._parents._belongsLinks, function(belongsLinks, key) {
    for(var i=0; i<belongsLinks[key].length; i++) {
      var parentDoc = belongsLinks[key][i].doc;
      var field = belongsLinks[key][i].key;
      for(var j=0; j<parentDoc[field].length; j++) {
        if (parentDoc[field][j] === this) {
          parentDoc[field].splice(j, 1);
          break;
        }
      }
    }
  });

  // Purge the database
  var promises = [];
  util.loopKeys(self._getModel()._joins, function(joins, field) {
    var join = joins[field];
    var joinedModel = join.model;

    if ((join.type === 'hasOne') || (join.type === 'hasMany')) {
      promises.push(r.table(joinedModel.getTableName()).getAll(self[join.leftKey], {index: join.rightKey}).replace(function(doc) {
        return doc.without(join.rightKey)
      }).run())
    }
    // nothing to do for "belongsTo"
    else if (join.type === 'hasAndBelongsToMany') {
      if (self.getModel()._getModel()._pk === join.leftKey) {
        // [1]
        promises.push(r.table(join.link).getAll(self[join.leftKey], {index: self.getModel().getTableName()+"_"+join.leftKey}).delete
().run())
      }
    }
  });

  util.loopKeys(self._getModel()._reverseJoins, function(reverseJoins, field) {
    var join = reverseJoins[field];
    var joinedModel = join.model; // model where belongsTo/hasAndBelongsToMany was called

    if (join.type === 'belongsTo') {
      // What was called is joinedModel.belongsTo(self, fieldDoc, leftKey, rightKey)
      promises.push(r.table(joinedModel.getTableName()).getAll(self[join.rightKey], {index: join.leftKey}).replace(function(doc) {
        return doc.without(join.leftKey)
      }).run())
    }
    // nothing to do for "belongsTo"
    else if (join.type === 'hasAndBelongsToMany') {
      // Purge only if the key is a primary key
      // What was called is joinedModel.hasAndBelongsToMany(self, fieldDoc, leftKey, rightKey)
      if (self.getModel()._getModel()._pk === join.leftKey) {
        promises.push(r.table(join.link).getAll(self[join.rightKey], {index: self.getModel().getTableName()+"_"+join.rightKey}).
delete().run())
      }
    }
  });

  // Delete itself
  promises.push(self.delete())

  return new Promise(function(resolve, reject) {
    Promise.all(promises).then(function() {
      resolve(self);
    }).error(reject);
  }).nodeify(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.removeRelation"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>removeRelation ()](#apidoc.element.thinky.document.prototype.removeRelation)
- description and source-code
```javascript
removeRelation = function () {
  var self = this;
  var pk = self._getModel()._pk;

  var query = self.getModel().get(this[pk])
  return query.removeRelation.apply(query, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.document.prototype.save"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>save (callback)](#apidoc.element.thinky.document.prototype.save)
- description and source-code
```javascript
save = function (callback) {
  return this._save({}, false, {}, callback);
}
```
- example usage
```shell
...
        }).error(reject);
      }))
    })(key);
  }
  else if ((deleteSelf === true) && (deletedDocs.indexOf(self[key]) === -1)) {
    delete self[key][joins[key].rightKey];
    if (self[key].isSaved() === true) {
      promises.push(self[key].save({}, false, {}, true, false));
    }
  }
}
if ((joins[key].type === 'belongsTo') && (self[key] instanceof Document)) {
  if ((self[key].isSaved() === true) &&
    ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key]) === -1)))) {
...
```

#### <a name="apidoc.element.thinky.document.prototype.saveAll"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>saveAll (docToSave, callback)](#apidoc.element.thinky.document.prototype.saveAll)
- description and source-code
```javascript
saveAll = function (docToSave, callback) {
  var saveAll;
  if (typeof docToSave === 'function') {
    callback = docToSave;
    saveAll = true;
    docToSave = {};
  }
  else {
    saveAll = docToSave === undefined;
    docToSave = docToSave || {};
  }

  return this._save(docToSave, saveAll,{}, callback);
}
```
- example usage
```shell
...
email: "orphee@gmail.com"
});

// Join the documents
post.author = author;


post.saveAll().then(function(result) {
/*
post = result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.document.prototype.setSaved"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>setSaved (all)](#apidoc.element.thinky.document.prototype.setSaved)
- description and source-code
```javascript
setSaved = function (all) {
  var self = this;
  self.__proto__._saved = true;
  if (all !== true) return;
    util.loopKeys(self._getModel()._joins, function(joins, key) {
      switch (joins[key].type) {
        case 'hasOne':
          if (self[key] instanceof Document) {
            self[key].setSaved(true);
          }
          break;

        case 'belongsTo':
          if (self[key] instanceof Document) {
            self[key].setSaved(true);
          }
          break;

        case 'hasMany':
          if (Array.isArray(self[key])) {
            for(var i=0; i<self[key].length; i++) {
              if (self[key][i] instanceof Document) {
                self[key][i].setSaved(true);
              }
            }
          }
          break;

        case 'hasAndBelongsToMany':
          if (Array.isArray(self[key])) {
            for(var i=0; i<self[key].length; i++) {
              if (self[key][i] instanceof Document) {
                self[key][i].setSaved(true);
              }
            }
          }
          break;
      }
    });

    // Make joins, we should keep references only of the saved documents
    util.loopKeys(self._getModel()._joins, function(joins, key) {
      if (self[key] == null) return;
      switch (joins[key].type) {
        case 'hasOne':
          if (self[key].isSaved()) {
            self.__proto__._hasOne[key] = {
              doc: self[key],
              foreignKey: self._getModel()._joins[key].rightKey
            }
          }

          if (self[key].__proto__._parents._hasOne[self._getModel()._name] == null) {
            self[key].__proto__._parents._hasOne[self._getModel()._name] = [];
          }
          self[key].__proto__._parents._hasOne[self._getModel()._name].push({
            doc: self,
            key: key
          });
          break;

        case 'belongsTo':
          if (self[key].__proto__._parents._belongsTo[self._getModel()._name] == null) {
            self[key].__proto__._parents._belongsTo[self._getModel()._name] = [];
          }
          self[key].__proto__._parents._belongsTo[self._getModel()._name].push({
            doc: self,
            foreignKey: self._getModel()._joins[key].leftKey,
            key: key
          });
          self.__proto__._belongsTo[key] = true;
          break;

        case 'hasMany':
          self.__proto__._hasMany[key] = []

          for(var i=0; i<self[key].length; i++) {
            if (self[key][i].isSaved()) {
              self.__proto__._hasMany[key].push({
                doc: self[key][i],
                foreignKey: self._getModel()._joins[key].rightKey
              })
            }

            if (self[key][i].__proto__._parents._hasMany[self._getModel()._name] == null) {
              self[key][i].__proto__._parents._hasMany[self._getModel()._name] = [];
            }
            self[key][i].__proto__._parents._hasMany[self._getModel()._name].push({
              doc: self,
              key: key
            });

          }
          break;

        case 'hasAndBelongsToMany':
          if (self.__proto__._links[self._getModel()._joins[key].link] === undefined) {
            self.__proto__._links[self._getModel()._joins[key].link] = {}
          }

          for(var i=0; i<self[key].length; i++) {
            if (self[key][i].isSaved()) {
              self.__proto__._links[self._getModel()._joins[key].link][self[key][i][self._getModel()._joins[key].rightKey]] = true
;
            }

            if (self[key][i].__proto__._parents._belongsLinks[self._getModel()._name] == null) {
              self[key][i].__proto__._parents._belongsLinks[self._getModel()._name] = [];
            }
            self[key][i].__proto__._parents._belongsLinks[self._getModel()._name].push({
              doc: self,
              key: key
            });

          }
          break;
      }
    });

}
```
- example usage
```shell
...
  self._merge(result.changes[0].new_val);
  self._setOldValue(util.deepCopy(result.changes[0].old_val));
}

if (self._getModel().needToGenerateFields === true) {
  self._generateDefault();
}
self.setSaved();
self.emit('saved', self);

var promise = self.validate();
if (promise instanceof Promise) {
  promise.then(function() {
    self._saveMany(docToSave, saveAll, savedModel, resolve, reject)
  }).error(reject);
...
```

#### <a name="apidoc.element.thinky.document.prototype.validate"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>validate (options, modelToValidate, validateAll, validatedModel, prefix)](#apidoc.element.thinky.document.prototype.validate)
- description and source-code
```javascript
validate = function (options, modelToValidate, validateAll, validatedModel, prefix) {
  modelToValidate = modelToValidate || {};
  validateAll = validateAll || false;
  validatedModel = validatedModel || {};
  prefix = prefix || '';

  var self = this;
  var validatedModelCopy = util.deepCopy(validatedModel);

  //TODO: Can we not always call this?
  var async = self._validateIsAsync(modelToValidate, validateAll, validatedModelCopy);

  return util.hook({
    preHooks: self._getModel()._pre.validate,
    postHooks: self._getModel()._post.validate,
    doc: self,
    async: async,
    fn: self._validateHook,
    fnArgs: [options, modelToValidate, validateAll, validatedModel, prefix]
  })
}
```
- example usage
```shell
...
* @param {Object=} modelToValidate Internal parameter, model to validate
* @return {Promise=} return a promise if the validation is asynchrone, else undefined.
*/
Document.prototype.validateAll = function(options, modelToValidate) {
 var validateAll = modelToValidate === undefined;
 modelToValidate = modelToValidate || {};

 return this.validate(options, modelToValidate, validateAll, {}, '', true);
}


/*
* Internal methods that will validate the document (but that will not execute the hooks).
* @param {Object=} options Options to overwrite the ones of the document.
* @param {Object=} modelToValidate Internal parameter, model to validate
...
```

#### <a name="apidoc.element.thinky.document.prototype.validateAll"></a>[function <span class="apidocSignatureSpan">thinky.document.prototype.</span>validateAll (options, modelToValidate)](#apidoc.element.thinky.document.prototype.validateAll)
- description and source-code
```javascript
validateAll = function (options, modelToValidate) {
  var validateAll = modelToValidate === undefined;
  modelToValidate = modelToValidate || {};

  return this.validate(options, modelToValidate, validateAll, {}, '', true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.errors"></a>[module thinky.errors](#apidoc.module.thinky.errors)

#### <a name="apidoc.element.thinky.errors.DocumentNotFound"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>DocumentNotFound (message)](#apidoc.element.thinky.errors.DocumentNotFound)
- description and source-code
```javascript
DocumentNotFound = function (message) {
  var errorMessage = message || "The query did not find a document and returned null.";
  errors.ThinkyError.call(this, errorMessage);
  this.name = 'DocumentNotFoundError';
}
```
- example usage
```shell
...
/**
 * Creates an appropriate error given either an instance of Error or a message
 * from the RethinkDB driver
 */
errors.create = function(errorOrMessage) {
var message = (errorOrMessage instanceof Error) ? errorOrMessage.message : errorOrMessage;
if (message.match(errors.DOCUMENT_NOT_FOUND_REGEX)) {
  return new errors.DocumentNotFound(message);
} else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
  var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
  return new errors.DuplicatePrimaryKey(message, primaryKey);
} else if (errorOrMessage instanceof Error) {
  return errorOrMessage;
}
...
```

#### <a name="apidoc.element.thinky.errors.DuplicatePrimaryKey"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>DuplicatePrimaryKey (message, primaryKey)](#apidoc.element.thinky.errors.DuplicatePrimaryKey)
- description and source-code
```javascript
DuplicatePrimaryKey = function (message, primaryKey) {
  errors.ThinkyError.call(this, message);
  this.name = 'DuplicatePrimaryKeyError';
  if (primaryKey !== undefined) {
    this.primaryKey = primaryKey;
  }
}
```
- example usage
```shell
...
 */
errors.create = function(errorOrMessage) {
  var message = (errorOrMessage instanceof Error) ? errorOrMessage.message : errorOrMessage;
  if (message.match(errors.DOCUMENT_NOT_FOUND_REGEX)) {
    return new errors.DocumentNotFound(message);
  } else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
    var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
    return new errors.DuplicatePrimaryKey(message, primaryKey);
  } else if (errorOrMessage instanceof Error) {
    return errorOrMessage;
  }

  return new errors.ThinkyError(errorOrMessage);
};
...
```

#### <a name="apidoc.element.thinky.errors.InvalidWrite"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>InvalidWrite (message, raw)](#apidoc.element.thinky.errors.InvalidWrite)
- description and source-code
```javascript
InvalidWrite = function (message, raw) {
  errors.ThinkyError.call(this, message);
  this.name = 'InvalidWriteError';
  this.raw = raw;
}
```
- example usage
```shell
...
Query.prototype._validateUngroupResult = function(result) {
}

Query.prototype._validateQueryResult = function(result) {
var self = this;
if (result.errors > 0) {
  console.log(result);
  return Promise.reject(new Errors.InvalidWrite("An error occured during the write", result));
}
if (!Array.isArray(result.changes)) {
  if (self._isPointWrite()) {
    return Promise.resolve();
  }
  return Promise.resolve([]);
}
...
```

#### <a name="apidoc.element.thinky.errors.ThinkyError"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>ThinkyError ()](#apidoc.element.thinky.errors.ThinkyError)
- description and source-code
```javascript
ThinkyError = function () {
  var tmp = Error.apply(this, arguments);
  tmp.name = this.name = 'ThinkyError';

  this.message = tmp.message;
  if (Error.captureStackTrace)
    Error.captureStackTrace(this, this.constructor);
}
```
- example usage
```shell
...
  } else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
    var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
    return new errors.DuplicatePrimaryKey(message, primaryKey);
  } else if (errorOrMessage instanceof Error) {
    return errorOrMessage;
  }

  return new errors.ThinkyError(errorOrMessage);
};
...
```

#### <a name="apidoc.element.thinky.errors.ValidationError"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>ValidationError (message)](#apidoc.element.thinky.errors.ValidationError)
- description and source-code
```javascript
ValidationError = function (message) {
  errors.ThinkyError.call(this, message);
  this.name = 'ValidationError';
}
```
- example usage
```shell
...
else {
  schemaOptions = options;
}


if (typeof self._getModel()._validator === 'function') {
  if (self._getModel()._validator.call(self, self) === false) {
    throw new Errors.ValidationError("Document's validator returned 'false'.");
  }
}

// Validate this document
self._getModel()._schema.validate(self, prefix, schemaOptions)

if (util.isPlainObject(modelToValidate) === false) {
...
```

#### <a name="apidoc.element.thinky.errors.create"></a>[function <span class="apidocSignatureSpan">thinky.errors.</span>create (errorOrMessage)](#apidoc.element.thinky.errors.create)
- description and source-code
```javascript
create = function (errorOrMessage) {
  var message = (errorOrMessage instanceof Error) ? errorOrMessage.message : errorOrMessage;
  if (message.match(errors.DOCUMENT_NOT_FOUND_REGEX)) {
    return new errors.DocumentNotFound(message);
  } else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
    var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
    return new errors.DuplicatePrimaryKey(message, primaryKey);
  } else if (errorOrMessage instanceof Error) {
    return errorOrMessage;
  }

  return new errors.ThinkyError(errorOrMessage);
}
```
- example usage
```shell
...
 * @param {Function} reject The function to call if an error happened
 */
Document.prototype._onSaved = function(result, docToSave, saveAll, savedModel, resolve, reject) {
// Keep in sync with Model.save
var self = this;

if (result.first_error != null) {
  return reject(Errors.create(result.first_error));
}

util.tryCatch(function() { // Validate the doc, replace it, and tag it as saved
  if (Array.isArray(result.changes) && result.changes.length > 0) {
    self._merge(result.changes[0].new_val);
    self._setOldValue(util.deepCopy(result.changes[0].old_val));
  }
...
```



# <a name="apidoc.module.thinky.feed"></a>[module thinky.feed](#apidoc.module.thinky.feed)

#### <a name="apidoc.element.thinky.feed.feed"></a>[function <span class="apidocSignatureSpan">thinky.</span>feed (feed, model)](#apidoc.element.thinky.feed.feed)
- description and source-code
```javascript
function Feed(feed, model) {
  this.feed = feed;
  this.model = model;
  this._closed = false;

  this.each = this._each;
  this.next = this._next;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.feed.prototype"></a>[module thinky.feed.prototype](#apidoc.module.thinky.feed.prototype)

#### <a name="apidoc.element.thinky.feed.prototype._each"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_each (callback, onFinish)](#apidoc.element.thinky.feed.prototype._each)
- description and source-code
```javascript
_each = function (callback, onFinish) {
  var self = this;
  self.feed.each(function(err, data) {
    if (err) {
      if (self._closed === true) {
        return;
      }
      return callback(err);
    }
    util.tryCatch(function() {
      if (data.new_val != null) {
        self.model._parse(data.new_val).then(function(doc) {
          doc._setOldValue(data.old_val);
          callback(null, doc);
        }).error(function(err) {
          callback(err);
        });
      }
      else if (data.old_val != null) { // new_val is null
        self.model._parse(data.old_val).then(function(doc) {
          doc._setUnSaved();
          callback(null, doc);
        }).error(function(err) {
          callback(err);
        });
      }
      //else we just drop the change as it's a state/initializing object
    }, function(err) {
      callback(err);
    })
  }, onFinish);
}
```
- example usage
```shell
...
(function(n) {
  var method = methods[n];
  Feed.prototype[method] = function() {
    var self = this;
    if (self._eventEmitter == null) {
      self._makeEmitter();
      setImmediate(function() {
        self.feed._each(self._eachCb.bind(self), function() {
          self._eventEmitter.emit('end');
        });
      });
    }
    self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
  };
})(i);
...
```

#### <a name="apidoc.element.thinky.feed.prototype._eachCb"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_eachCb (err, data)](#apidoc.element.thinky.feed.prototype._eachCb)
- description and source-code
```javascript
_eachCb = function (err, data) {
  var self = this;
  if (err != null) {
    if ((this._closed !== false) || (err.message !== "You cannot retrieve data from a cursor that is closed")) {
      self._eventEmitter.emit('error', err);
    }
    return;
  }

  util.tryCatch(function() {
    if (data.new_val !== null) {
      self.model._parse(data.new_val).then(function(doc) {
        doc._setOldValue(data.old_val);
        self._eventEmitter.emit('data', doc);
      }).error(function(err) {
        self._eventEmitter.emit('error', err);
      });
    }
    else if (data.old_val !== null) { // new_val is null
      self.model._parse(data.old_val).then(function(doc) {
        doc._setUnSaved();
        self._eventEmitter.emit('data', doc);
      }).error(function(err) {
        self._eventEmitter.emit('error', err);
      });
    }
  }, function(err) {
    self._eventEmitter.emit('error', err);
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype._makeEmitter"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_makeEmitter ()](#apidoc.element.thinky.feed.prototype._makeEmitter)
- description and source-code
```javascript
_makeEmitter = function () {
  this.next = function() {
    throw new Error("You cannot called 'next' once you have bound listeners on the feed")
  }
  this.each = function() {
    throw new Error("You cannot called 'each' once you have bound listeners on the feed")
  }
  this.toArray = function() {
    throw new Error("You cannot called 'toArray' once you have bound listeners on the feed")
  }
  this._eventEmitter = new EventEmitter();
}
```
- example usage
```shell
...

for(var i=0; i<methods.length; i++) {
(function(n) {
  var method = methods[n];
  Feed.prototype[method] = function() {
    var self = this;
    if (self._eventEmitter == null) {
      self._makeEmitter();
      setImmediate(function() {
        self.feed._each(self._eachCb.bind(self), function() {
          self._eventEmitter.emit('end');
        });
      });
    }
    self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
...
```

#### <a name="apidoc.element.thinky.feed.prototype._next"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>_next ()](#apidoc.element.thinky.feed.prototype._next)
- description and source-code
```javascript
_next = function () {
  var self = this;
  return new Promise(function(resolve, reject) {
    self.feed.next().then(function(data) {
      util.tryCatch(function() {
        if (data.new_val != null) {
          self.model._parse(data.new_val).then(function(doc) {
            doc._setOldValue(data.old_val);
            resolve(doc);
          }).error(reject);
        }
        else if (data.old_val != null) { // new_val is null
          self.model._parse(data.old_val).then(function(doc) {
            doc._setUnSaved();
            resolve(doc);
          }).error(reject);
        }
        //else we just drop the change as it's a state/initializing object
      }, function(err) {
        reject(err);
      })
    }).error(reject);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.addListener"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>addListener ()](#apidoc.element.thinky.feed.prototype.addListener)
- description and source-code
```javascript
addListener = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
...
  _belongsLinks: {} // <tableName>: [{doc, key}]
}

// Bind listeners of the model to this documents.
util.loopKeys(model._listeners, function(listeners, eventKey) {
  for(var j=0; j<listeners[eventKey].length; j++) {
    if (listeners[eventKey][j].once === false) {
      self.addListener(eventKey, listeners[eventKey][j].listener);
    }
    else if (listeners[eventKey][j].once === true) {
      self.once(eventKey, listeners[eventKey][j].listener);
    }
  }
});
...
```

#### <a name="apidoc.element.thinky.feed.prototype.close"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>close (callback)](#apidoc.element.thinky.feed.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  this._closed = true;
  return this.feed.close(callback);
}
```
- example usage
```shell
...
};

Document.prototype.getFeed = function() {
  return this.__proto__._feed;
}

Document.prototype.closeFeed = function() {
  return this.__proto__._feed.close();
}

/**
 * Have the model emit 'retrieved' with the current document and
 * recurse to have all joined models do the same.
 */
Document.prototype._emitRetrieve = function() {
...
```

#### <a name="apidoc.element.thinky.feed.prototype.emit"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>emit ()](#apidoc.element.thinky.feed.prototype.emit)
- description and source-code
```javascript
emit = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
...
 * @param {Object=} savedModel Models saved in this call
 * @param {Object=} callback to execute
 * @return {Promise=}
 */
Document.prototype._save = function(docToSave, saveAll, savedModel, callback) {
//TOIMPROVE? How should we handle circular references outsides of joined fields? Now we throw with a maximum call stack size exceed
var self = this;
self.emit('saving', self);

return util.hook({
  preHooks: self._getModel()._pre.save,
  postHooks: self._getModel()._post.save,
  doc: self,
  async: true,
  fn: self._saveHook,
...
```

#### <a name="apidoc.element.thinky.feed.prototype.listeners"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>listeners ()](#apidoc.element.thinky.feed.prototype.listeners)
- description and source-code
```javascript
listeners = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.on"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>on ()](#apidoc.element.thinky.feed.prototype.on)
- description and source-code
```javascript
on = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.once"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>once ()](#apidoc.element.thinky.feed.prototype.once)
- description and source-code
```javascript
once = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
...
// Bind listeners of the model to this documents.
util.loopKeys(model._listeners, function(listeners, eventKey) {
  for(var j=0; j<listeners[eventKey].length; j++) {
    if (listeners[eventKey][j].once === false) {
      self.addListener(eventKey, listeners[eventKey][j].listener);
    }
    else if (listeners[eventKey][j].once === true) {
      self.once(eventKey, listeners[eventKey][j].listener);
    }
  }
});


// Atom feed
this._active = false;
...
```

#### <a name="apidoc.element.thinky.feed.prototype.removeAllListeners"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>removeAllListeners ()](#apidoc.element.thinky.feed.prototype.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.removeListener"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>removeListener ()](#apidoc.element.thinky.feed.prototype.removeListener)
- description and source-code
```javascript
removeListener = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.setMaxListeners"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>setMaxListeners ()](#apidoc.element.thinky.feed.prototype.setMaxListeners)
- description and source-code
```javascript
setMaxListeners = function () {
  var self = this;
  if (self._eventEmitter == null) {
    self._makeEmitter();
    setImmediate(function() {
      self.feed._each(self._eachCb.bind(self), function() {
        self._eventEmitter.emit('end');
      });
    });
  }
  self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.feed.prototype.toArray"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>toArray ()](#apidoc.element.thinky.feed.prototype.toArray)
- description and source-code
```javascript
toArray = function () {
  throw new Error("The 'toArray' method is not available on feeds.");
}
```
- example usage
```shell
...
        self._makeEmitter();
        setImmediate(function() {
          self.feed._each(self._eachCb.bind(self), function() {
            self._eventEmitter.emit('end');
          });
        });
      }
      self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
    };
  })(i);
}

module.exports = Feed;
...
```

#### <a name="apidoc.element.thinky.feed.prototype.toString"></a>[function <span class="apidocSignatureSpan">thinky.feed.prototype.</span>toString ()](#apidoc.element.thinky.feed.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return '[object Feed]'
}
```
- example usage
```shell
...
}

/**
 * Convert the query to its string representation.
 * @return {string}
 */
Query.prototype.toString = function() {
  return this._query.toString();
}

module.exports = Query;
...
```



# <a name="apidoc.module.thinky.model"></a>[module thinky.model](#apidoc.module.thinky.model)

#### <a name="apidoc.element.thinky.model.model"></a>[function <span class="apidocSignatureSpan">thinky.</span>model (name, schema, options, thinky)](#apidoc.element.thinky.model.model)
- description and source-code
```javascript
function Model(name, schema, options, thinky) {
<span class="apidocCodeCommentSpan">  /**
   * Name of the table used
   * @type {string}
   */
</span>  this._name = name;

  // We want a deep copy
  options = options || {};
  this._options = {};
  this._options.enforce_missing = (options.enforce_missing != null) ? options.enforce_missing : thinky._options.enforce_missing;
  this._options.enforce_extra = (options.enforce_extra != null) ? options.enforce_extra : thinky._options.enforce_extra;
  this._options.enforce_type = (options.enforce_type != null) ? options.enforce_type : thinky._options.enforce_type;
  this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : thinky._options.timeFormat;
  this._options.validate = (options.validate != null) ? options.validate : thinky._options.validate;

  this._schema = schemaUtil.parse(schema, '', this._options, this);
  //console.log(JSON.stringify(this._schema, null, 2));

  this.virtualFields = [];
  this.defaultFields = [];
  this._schema._getDefaultFields([], this.defaultFields, this.virtualFields)

  this.needToGenerateFields = (this.defaultFields.length+this.virtualFields.length) !== 0;

  this._pk = (options.pk != null) ? options.pk : 'id';

  this._table = (options.table != null) ? options.table : {};
  this._table.primaryKey = this._pk;

  this._thinky = thinky;

  this._validator = options.validator;

  this._indexes = {}; // indexName -> true
  this._pendingPromises = [];

  this._error = null; // If an error occured, we won't let people save things

  this._listeners = {};
  this._maxListeners = 10;
  this._joins = {};
  this._localKeys = {}; // key used as a foreign key by another model

  // This is to track joins that were not directly called by this model but that we still need
  // to purge the database
  this._reverseJoins = {};

  this._methods = {};
  this._staticMethods = {};
  this._async = {
    init: false,
    retrieve: false,
    save: false,
    validate: false
  };

  this._pre = {
    save: [],
    delete: [],
    validate: []
  };
  this._post = {
    init: [],
    retrieve: [],
    save: [],
    delete: [],
    validate: []
  };
}
```
- example usage
```shell
...
  util.loopKeys(self._getModel()._joins, function(joins, key) {
if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
  switch (joins[key].type) {
    case 'hasOne':
    case 'belongsTo':
      if (util.isPlainObject(self[key])) {
        if (self[key] instanceof Document === false) {
          self[key] = new self._getModel()._joins[key].model(self[key]);
        }
        // We do not propagate the options of this document, but only those given to validate
        var promise = self[key].validate(options, modelToValidate[key], validateAll, validatedModel, prefix+'['+key+']');
        if (promise instanceof Promise) {
          promises.push(promise);
          promise = null;
        }
...
```

#### <a name="apidoc.element.thinky.model.new"></a>[function <span class="apidocSignatureSpan">thinky.model.</span>new (name, schema, options, thinky)](#apidoc.element.thinky.model.new)
- description and source-code
```javascript
new = function (name, schema, options, thinky) {

  var proto = new Model(name, schema, options, thinky);
  proto._initModel = options.init  !== undefined ? !!options.init : true;

  var model = function model(doc, options) {
    if (!util.isPlainObject(doc)) {
      throw new Error("Cannot build a new instance of '"+proto._name+"' without an object")
    }
    // We create a deepcopy only if doc was already used to create a document
    if (doc instanceof Document) {
      doc = util.deepCopy(doc);
    }

    util.changeProto(doc, new Document(model, options));

    // Create joins document. We do it here because 'options' are easily available
    util.loopKeys(proto._joins, function(joins, key) {
      if (doc[key] != null) {
        if ((joins[key].type === 'hasOne') && (doc[key] instanceof Document === false)) {
          doc[key] = new joins[key].model(doc[key], options);
        }
        else if ((joins[key].type === 'belongsTo') && (doc[key] instanceof Document === false)) {
          doc[key] = new joins[key].model(doc[key], options);
        }
        else if (joins[key].type === 'hasMany') {
          doc.__proto__._hasMany[key] = []

          for(var i=0; i<doc[key].length; i++) {
            if (doc[key][i] instanceof Document === false) {
              doc[key][i] = new joins[key].model(doc[key][i], options);
            }
          }
        }
        else if (joins[key].type === 'hasAndBelongsToMany') {
          for(var i=0; i<doc[key].length; i++) {
            if (doc[key][i] instanceof Document === false) {
              doc[key][i] = new joins[key].model(doc[key][i], options);
            }
          }
        }
      }
    });
    doc._getModel()._schema._setModel(doc._getModel());
    if (proto.needToGenerateFields === true) {
      doc._generateDefault();
    }

    var promises = [];
    var promise;
    if (proto._options.validate === 'oncreate') {
      promise = doc.validate(options);
      if (promise instanceof Promise) promises.push(promise);
    }

    if (proto._post.init.length > 0) {
      promise = util.hook({
        postHooks: doc._getModel()._post.init,
        doc: doc,
        async: doc._getModel()._async.init,
        fn: function() {
          return doc;
        }
      })
      if (promise instanceof Promise) promises.push(promise);
    }

    if (promises.length > 0) {
      return Promise.all(promises).then(function(docs) {
        return docs[0];
      });
    }
    return doc;
  }

  model.__proto__ = proto;

  if (options.init !== false) {
    // Setup the model's table.
    model.tableReady().then();
  }
  else {
    // We do not initialize the table and suppose that it already exists and
    // is ready.
    model.emit('created');
    model.emit('ready');
  }

  // So people can directly call the EventEmitter from the constructor
  // TOIMPROVE: We should emit everything from the constructor instead of emitting things from
  // the constructor and the instance of Model
  util.loopKeys(EventEmitter.prototype, function(emitter, key) {
    (function(_key) {
      model[_key] = function() {
        model._getModel()[_key].apply(model._getModel(), arguments);
      }
    })(key)
  });


  return model
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.super_"></a>[function <span class="apidocSignatureSpan">thinky.model.</span>super_ ()](#apidoc.element.thinky.model.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.model.prototype"></a>[module thinky.model.prototype](#apidoc.module.thinky.model.prototype)

#### <a name="apidoc.element.thinky.model.prototype.ISO8601"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ISO8601 ()](#apidoc.element.thinky.model.prototype.ISO8601)
- description and source-code
```javascript
ISO8601 = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype._createIndex"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_createIndex (name, fn, opts)](#apidoc.element.thinky.model.prototype._createIndex)
- description and source-code
```javascript
_createIndex = function (name, fn, opts) {
  var model = this._getModel();
  var tableName = this.getTableName();
  var r = model._thinky.r;

  if (opts === undefined && util.isPlainObject(fn)) {
    opts = fn;
    fn = undefined;
  }

  var promise = this.tableReady().then(function() {
    return new Promise(function(resolve, reject) {
      return r.branch(
        r.table(tableName).indexList().contains(name),
        r.table(tableName).indexWait(name),
        r.branch(
          r.table(tableName).info()('primary_key').eq(name),
          r.table(tableName).indexWait(name),
          r.table(tableName).indexCreate(name, fn, opts).do(function() {
            return r.table(tableName).indexWait(name);
          })
        )
      )
      .run()
      .then(resolve)
      .error(function(error) {
        if (error.message.match(/^Index/)) {
          // TODO: This regex seems a bit too generous since messages such
          // as "Index 'id' was not found on table..." will be accepted.
          // Figure out if this is OK or not.
          return resolve();
        }
        reject(error);
      });
    });
  })
  .then(function() {
    model._indexes[name] = true;
  });

  this._waitFor(promise);
  return promise;
}
```
- example usage
```shell
...
  var self = this;

  if ((opts === undefined) && (util.isPlainObject(fn))) {
    opts = fn;
    fn = undefined;
  }

  return self._createIndex(name, fn, opts)
  .catch(function(error) {
    self._getModel()._setError(error);
    throw error;
  });
}

Model.prototype._createIndex = function(name, fn, opts) {
...
```

#### <a name="apidoc.element.thinky.model.prototype._get"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_get ()](#apidoc.element.thinky.model.prototype._get)
- description and source-code
```javascript
_get = function () {
  var query = new Query(this);
  query = query['_get'].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype._getModel"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_getModel ()](#apidoc.element.thinky.model.prototype._getModel)
- description and source-code
```javascript
_getModel = function () {
  return this.__proto__;
}
```
- example usage
```shell
...
 * @param {function} model The model of this document
 * @param {object=} options Options that can overwrite the ones of the model
 */
function Document(model, options) {
var self = this;  // Keep a reference to itself.

this.constructor = model;  // The constructor for this model
this._model = model._getModel(); // The instance of Model

// We don't want to store options if they are different
// than the one provided by the model
if (util.isPlainObject(options)) {
  this._schemaOptions = {};
  this._schemaOptions.enforce_missing =
      (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
...
```

#### <a name="apidoc.element.thinky.model.prototype._parse"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_parse (data, ungroup)](#apidoc.element.thinky.model.prototype._parse)
- description and source-code
```javascript
_parse = function (data, ungroup) {
  var self = this;
  var promises = [];
  var promise;

  var p = new Promise(function(resolve, reject) {
    if (ungroup) {
      for(var i=0; i<data.length; i++) {
        for(var j=0; j<data[i].reduction.length; j++) {
          util.tryCatch(function() {
            var newDoc = new self(data[i].reduction[j]);
            newDoc.setSaved(true);
            newDoc._emitRetrieve();
            data[i].reduction[j] = newDoc;
          }, reject)
        }
      }
      return resolve(data);
    }
    else if (Array.isArray(data)) {
      util.tryCatch(function() {
        for(var i=0; i<data.length; i++) {
          data[i] = new self(data[i])
          data[i].setSaved(true);

          self.emit('retrieved', data[i]);

          (function(i) {
            // Order matters here, we want the hooks to be executed *before* calling validate
            promise = util.hook({
              postHooks: data[i]._getModel()._post.retrieve,
              doc: data[i],
              async: data[i]._getModel()._async.retrieve,
              fn: function() {}
            })
            if (promise instanceof Promise) {
              promise.then(function() {
                var promise = data[i].validate();
                if (promise instanceof Promise) {
                  promise.then(function() {
                    resolve(data)
                  }).error(reject);
                }
                else {
                  resolve(data);
                }
              }).error(reject);
              promises.push(promise);
            }
            else {
              promise = data[i].validate();
              if (promise instanceof Promise) promises.push(promise);
            }
          })(i);
        }
      }, function(error) {
        var newError = new Error("The results could not be converted to instances of '"+self.getTableName()+"'\nDetailed error: "+
error.message);

        return reject(newError);
      });

      if (promises.length > 0) {
        Promise.all(promises).then(function() {
          resolve(data);
        }).error(reject);
      }
      else {
        resolve(data);
      }
    }
    else {
      // If we get a GROUPED_DATA, we convert documents in each group
      if (util.isPlainObject(data) && (data.$reql_type$ === "GROUPED_DATA")) {
        var result = [];
        util.tryCatch(function() {
          var reduction, newDoc;
          for(var i=0; i<data.data.length; i++) {
            (function(i) {
              reduction = [];
              if (Array.isArray(data.data[i][1])) {
                for(var j=0; j<data.data[i][1].length; j++) {
                  (function(j) {
                    newDoc = new self(data.data[i][1][j]);
                    newDoc.setSaved(true);

                    newDoc._emitRetrieve();

                    promise = util.hook({
                      postHooks: newDoc._getModel()._post.retrieve,
                      doc: newDoc,
                      async: newDoc._getModel()._async.retrieve,
                      fn: function() {}
                    })
                    if (promise instanceof Promise) {
                      promise.then(function() {
                        var promise = newDoc.validate();
                        if (promise instanceof Promise) {
                          promise.then(function() {
                            resolve(data)
                          }).error(reject);
                        }
                        else {
                          resolve(data);
                        }
                      }).error(reject);
                      promises.push(promise);
                    }
                    else {
                      promise = newDoc.validate();
                      if (promise instanceof Promise) promises.push(promise);
                    }

                    reduction.push(newDoc)
                  })(j);
                }
                result.push({
                  group: data.data[i][0],
                  reduction: reduction
                })
              } ...
```
- example usage
```shell
...

Feed.prototype._next = function() {
var self = this;
return new Promise(function(resolve, reject) {
  self.feed.next().then(function(data) {
    util.tryCatch(function() {
      if (data.new_val != null) {
        self.model._parse(data.new_val).then(function(doc) {
          doc._setOldValue(data.old_val);
          resolve(doc);
        }).error(reject);
      }
      else if (data.old_val != null) { // new_val is null
        self.model._parse(data.old_val).then(function(doc) {
          doc._setUnSaved();
...
```

#### <a name="apidoc.element.thinky.model.prototype._promisesReady"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_promisesReady ()](#apidoc.element.thinky.model.prototype._promisesReady)
- description and source-code
```javascript
_promisesReady = function () {
  var self = this;
  if (this._promisesReadyPromise) return this._promisesReadyPromise;

  var verifyAll = function() {
    return Promise.all(self._pendingPromises)
    .then(function() {
      var i, allFullfilled = true;
      for (i=0; i<self._pendingPromises.length; i++) {
         if (!self._pendingPromises[i].isFulfilled()) {
          allFullfilled = false;
          break;
         }
      }
      return allFullfilled ? Promise.resolve() : verifyAll();
    });
  };

  this._promisesReadyPromise = verifyAll();
  return this._promisesReadyPromise;
}
```
- example usage
```shell
...
Model.prototype.ready = function() {
var requirements = [];

// Ensure the Model's table is ready
requirements.push(this.tableReady());

// Ensure all other pending promises have been resolved
requirements.push(this._promisesReady());

return Promise.all(requirements);
};

Model.prototype._promisesReady = function() {
var self = this;
if (this._promisesReadyPromise) return this._promisesReadyPromise;
...
```

#### <a name="apidoc.element.thinky.model.prototype._setError"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_setError (error)](#apidoc.element.thinky.model.prototype._setError)
- description and source-code
```javascript
_setError = function (error) {
  this._getModel()._error = error;
  this.emit('error', error);
}
```
- example usage
```shell
...
if ((opts === undefined) && (util.isPlainObject(fn))) {
  opts = fn;
  fn = undefined;
}

return self._createIndex(name, fn, opts)
.catch(function(error) {
  self._getModel()._setError(error);
  throw error;
});
}

Model.prototype._createIndex = function(name, fn, opts) {
var model = this._getModel();
var tableName = this.getTableName();
...
```

#### <a name="apidoc.element.thinky.model.prototype._waitFor"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>_waitFor (promise)](#apidoc.element.thinky.model.prototype._waitFor)
- description and source-code
```javascript
_waitFor = function (promise) {
  var self = this;
  this._pendingPromises.push(promise);

  // Emit 'ready' when all pending promises have resolved
  if (!this._pendingReady) {
    this._pendingReady = this._promisesReady().then(function() {
      delete self._pendingReady;
      self.emit('ready', self);
    });
  }
}
```
- example usage
```shell
...
     });
   });
 })
 .then(function() {
   model._indexes[name] = true;
 });

 this._waitFor(promise);
 return promise;
};

/*
* joinedModel: the joined model
* fieldDoc: the field where the joined document will be kept
* leftKey: the key in the model used for the join
...
```

#### <a name="apidoc.element.thinky.model.prototype.add"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>add ()](#apidoc.element.thinky.model.prototype.add)
- description and source-code
```javascript
add = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
      innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
      return r.branch(
        result.count().eq(1),
        r.object(key, innerQuery),
        r.branch(
          result.count().eq(0),
          {},
          r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
        )
      )
    }),
    {}
  )
});
break;
...
```

#### <a name="apidoc.element.thinky.model.prototype.and"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>and ()](#apidoc.element.thinky.model.prototype.and)
- description and source-code
```javascript
and = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.append"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>append ()](#apidoc.element.thinky.model.prototype.append)
- description and source-code
```javascript
append = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.april"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>april ()](#apidoc.element.thinky.model.prototype.april)
- description and source-code
```javascript
april = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.args"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>args ()](#apidoc.element.thinky.model.prototype.args)
- description and source-code
```javascript
args = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  }
}

// Replace all documents with string-type primary keys
// in a single replace() operation.
if (primaryKeys.length) {
  revertPromises.push(
    r.table(self._model.getTableName()).getAll(r.args(primaryKeys)).replace(function(doc) {
      return r.expr(keysToValues)(doc(self._model._pk));
    }).run()
  );
}

return Promise.all(revertPromises).then(function(result) {
  throw new Error("The write failed, and the changes were reverted.");
...
```

#### <a name="apidoc.element.thinky.model.prototype.asc"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>asc ()](#apidoc.element.thinky.model.prototype.asc)
- description and source-code
```javascript
asc = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.august"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>august ()](#apidoc.element.thinky.model.prototype.august)
- description and source-code
```javascript
august = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.avg"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>avg ()](#apidoc.element.thinky.model.prototype.avg)
- description and source-code
```javascript
avg = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.belongsTo"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>belongsTo (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.belongsTo)
- description and source-code
```javascript
belongsTo = function (joinedModel, fieldDoc, leftKey, rightKey, options) {
  var self  = this;

  if ((joinedModel instanceof Model) === false) {
    throw new Error("First argument of 'belongsTo' must be a Model")
  }
  if (fieldDoc in self._getModel()._joins) {
    throw new Error("The field '"+fieldDoc+"' is already used by another relation.");
  }
  if (fieldDoc === "_apply") {
    throw new Error("The field '_apply' is reserved by thinky. Please use another one.");
  }

  self._getModel()._joins[fieldDoc] = {
    model: joinedModel,
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'belongsTo'
  };
  self._getModel()._localKeys[leftKey] = true;

  joinedModel._getModel()._reverseJoins[fieldDoc] = {
    model: self,
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'belongsTo',
  }

  options = options || {};
  if (options.init !== false) {
<span class="apidocCodeCommentSpan">    /*
    var newIndex = self._createIndex(leftKey)
    .catch(function(error) {
      joinedModel._getModel()._setError(error);
      self._getModel()._setError(error);
    });
    joinedModel._waitFor(newIndex);
    */
</span>    var newIndex = joinedModel._createIndex(rightKey)
    .catch(function(error) {
      joinedModel._getModel()._setError(error);
      self._getModel()._setError(error);
    });
    self._waitFor(newIndex);

  }
}
```
- example usage
```shell
...
var Author = thinky.createModel("Author", {
  id: type.string(),      // a normal string
  name: type.string().min(2),  // a string of at least two characters
  email: type.string().email()  // a string that is a valid email
});

// Join the models
Post.belongsTo(Author, "author", "idAuthor", "id");
'''

Save a new post with its author.

'''js
// Create a new post
var post = new Post({
...
```

#### <a name="apidoc.element.thinky.model.prototype.between"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>between ()](#apidoc.element.thinky.model.prototype.between)
- description and source-code
```javascript
between = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.binary"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>binary ()](#apidoc.element.thinky.model.prototype.binary)
- description and source-code
```javascript
binary = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.bracket"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>bracket ()](#apidoc.element.thinky.model.prototype.bracket)
- description and source-code
```javascript
bracket = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  var updateValue = {};
  if (joinedDocument[joins[field].rightKey] === undefined) {
    if (joinedDocument[joinedModel._pk] === undefined) {
      return new Query(model, self, {},
          new Error('The primary key or the joined key must be defined in the joined document for a 'belongsTo' relation.')
      );
    }
    updateValue[joins[field].leftKey] = joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey)._query;
  }
  else {
    updateValue[joins[field].leftKey] = joinedDocument[joins[field].rightKey];
  }
  return self.update(updateValue, {nonAtomic: true}).run();
case 'hasAndBelongsToMany':
  var linkModel = joins[field].linkModel;
...
```

#### <a name="apidoc.element.thinky.model.prototype.branch"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>branch ()](#apidoc.element.thinky.model.prototype.branch)
- description and source-code
```javascript
branch = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
if (opts === undefined && util.isPlainObject(fn)) {
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
...
```

#### <a name="apidoc.element.thinky.model.prototype.catch"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>catch ()](#apidoc.element.thinky.model.prototype.catch)
- description and source-code
```javascript
catch = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

if ((opts === undefined) && (util.isPlainObject(fn))) {
  opts = fn;
  fn = undefined;
}

return self._createIndex(name, fn, opts)
.catch(function(error) {
  self._getModel()._setError(error);
  throw error;
});
}

Model.prototype._createIndex = function(name, fn, opts) {
var model = this._getModel();
...
```

#### <a name="apidoc.element.thinky.model.prototype.ceil"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ceil ()](#apidoc.element.thinky.model.prototype.ceil)
- description and source-code
```javascript
ceil = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.changeAt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>changeAt ()](#apidoc.element.thinky.model.prototype.changeAt)
- description and source-code
```javascript
changeAt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.changes"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>changes ()](#apidoc.element.thinky.model.prototype.changes)
- description and source-code
```javascript
changes = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
    }
  })(key);
  break;

case 'changes':
  (function(key) {
    Query.prototype[key] = function() {
      // In case of 'get().changes()' we want to remove the default(r.errror(...))
      // TODO: Do not hardcode this?
      if ((typeof this._query === 'function') && (this._query._query[0] === 92)) {
        this._query._query = this._query._query[1][0];
      }
      return new Query(this._model, this._query[key].apply(this._query, arguments));
    }
  })(key);
...
```

#### <a name="apidoc.element.thinky.model.prototype.circle"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>circle ()](#apidoc.element.thinky.model.prototype.circle)
- description and source-code
```javascript
circle = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.coerceTo"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>coerceTo ()](#apidoc.element.thinky.model.prototype.coerceTo)
- description and source-code
```javascript
coerceTo = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
...
```

#### <a name="apidoc.element.thinky.model.prototype.concatMap"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>concatMap ()](#apidoc.element.thinky.model.prototype.concatMap)
- description and source-code
```javascript
concatMap = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
          break;

        case 'hasAndBelongsToMany':
          self._query = self._query.merge(function(doc) {
            if ((model.getTableName() === joins[key].model.getTableName()) && (joins[key].leftKey === joins[key].rightKey)) {
// In case the model is linked with itself on the same key

innerQuery = r.table(joins[key].link).getAll(doc(joins[key].leftKey), {index: joins[key].leftKey+"_"+joins[key].leftKey}).concatMap
(function(link) {
  return r.table(joins[key].model.getTableName()).getAll(
    r.branch(
      doc(joins[key].leftKey).eq(link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)),
      link(joins[key].leftKey+"_"+joins[key].leftKey).nth(1),
      link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)
    )
  , {index: joins[key].rightKey})
...
```

#### <a name="apidoc.element.thinky.model.prototype.config"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>config ()](#apidoc.element.thinky.model.prototype.config)
- description and source-code
```javascript
config = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.contains"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>contains ()](#apidoc.element.thinky.model.prototype.contains)
- description and source-code
```javascript
contains = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
...
```

#### <a name="apidoc.element.thinky.model.prototype.count"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>count ()](#apidoc.element.thinky.model.prototype.count)
- description and source-code
```javascript
count = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
  result.count().eq(1),
  r.object(key, innerQuery),
  r.branch(
    result.count().eq(0),
    {},
    r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
  )
)
...
```

#### <a name="apidoc.element.thinky.model.prototype.date"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>date ()](#apidoc.element.thinky.model.prototype.date)
- description and source-code
```javascript
date = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  if (schema.integer === true) { result.integer(); }
  return result;
case Boolean:
  result = type.boolean().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
  return result;
case Date:
  var result = type.date().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
  if (schema.min instanceof Date) { result.min(schema.min); }
  if (schema.max instanceof Date) { result.max(schema.max); }
  return result;
case Buffer:
  result = type.buffer().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
...
```

#### <a name="apidoc.element.thinky.model.prototype.day"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>day ()](#apidoc.element.thinky.model.prototype.day)
- description and source-code
```javascript
day = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.dayOfWeek"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dayOfWeek ()](#apidoc.element.thinky.model.prototype.dayOfWeek)
- description and source-code
```javascript
dayOfWeek = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.dayOfYear"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dayOfYear ()](#apidoc.element.thinky.model.prototype.dayOfYear)
- description and source-code
```javascript
dayOfYear = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.db"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>db ()](#apidoc.element.thinky.model.prototype.db)
- description and source-code
```javascript
db = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.dbCreate"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbCreate ()](#apidoc.element.thinky.model.prototype.dbCreate)
- description and source-code
```javascript
dbCreate = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.dbDrop"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbDrop ()](#apidoc.element.thinky.model.prototype.dbDrop)
- description and source-code
```javascript
dbDrop = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.dbList"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>dbList ()](#apidoc.element.thinky.model.prototype.dbList)
- description and source-code
```javascript
dbList = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.december"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>december ()](#apidoc.element.thinky.model.prototype.december)
- description and source-code
```javascript
december = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.default"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>default ()](#apidoc.element.thinky.model.prototype.default)
- description and source-code
```javascript
default = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
// Note: We suppose that no method has an empty name
switch (key) {
  case 'get':
    // 'get' in thinky returns an error if the document is not found.
    // The driver currently just returns 'null'.
    (function(key) {
      Query.prototype[key] = function() {
        return new Query(this._model, this._query[key].apply(this._query, arguments)).default(this._r.error(new Errors.DocumentNotFound
().message));
      }
    })(key);
    // Copy it in '_get' without 'default'.
    (function(key) {
      Query.prototype['_get'] = function() {
        // Create a new query to let people fork it
        return new Query(this._model, this._query[key].apply(this._query, arguments));
...
```

#### <a name="apidoc.element.thinky.model.prototype.define"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>define (key, fn)](#apidoc.element.thinky.model.prototype.define)
- description and source-code
```javascript
define = function (key, fn) {
  this._methods[key] = fn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.defineStatic"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>defineStatic (key, fn)](#apidoc.element.thinky.model.prototype.defineStatic)
- description and source-code
```javascript
defineStatic = function (key, fn) {
  this._staticMethods[key] = fn;

  this[key] = function() {
    return fn.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.delay"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>delay ()](#apidoc.element.thinky.model.prototype.delay)
- description and source-code
```javascript
delay = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.delete"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>delete ()](#apidoc.element.thinky.model.prototype.delete)
- description and source-code
```javascript
delete = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
this._belongsTo = {};
this._hasOne = {};
this._hasMany = {};
// Example: { <linkTableName>: { <valueOfRightKey>: true, ... }, ... }
this._links = {}

// Keep reference of any doc having a link pointing to this
// So we can clean when users do doc.belongsToDoc.delete()
this._parents = {
  _hasOne: {},      // <tableName>: [{doc, key}]
  _hasMany: {},     // <tableName>: [{doc, key}]
  _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
  _belongsLinks: {} // <tableName>: [{doc, key}]
}
...
```

#### <a name="apidoc.element.thinky.model.prototype.deleteAt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>deleteAt ()](#apidoc.element.thinky.model.prototype.deleteAt)
- description and source-code
```javascript
deleteAt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.desc"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>desc ()](#apidoc.element.thinky.model.prototype.desc)
- description and source-code
```javascript
desc = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.difference"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>difference ()](#apidoc.element.thinky.model.prototype.difference)
- description and source-code
```javascript
difference = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.distance"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>distance ()](#apidoc.element.thinky.model.prototype.distance)
- description and source-code
```javascript
distance = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.distinct"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>distinct ()](#apidoc.element.thinky.model.prototype.distinct)
- description and source-code
```javascript
distinct = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.div"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>div ()](#apidoc.element.thinky.model.prototype.div)
- description and source-code
```javascript
div = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.do"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>do ()](#apidoc.element.thinky.model.prototype.do)
- description and source-code
```javascript
do = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
    return new Promise(function(resolve, reject) {
return r.branch(
  r.table(tableName).indexList().contains(name),
  r.table(tableName).indexWait(name),
  r.branch(
    r.table(tableName).info()('primary_key').eq(name),
    r.table(tableName).indexWait(name),
    r.table(tableName).indexCreate(name, fn, opts).do(function() {
      return r.table(tableName).indexWait(name);
    })
  )
)
.run()
.then(resolve)
.error(function(error) {
...
```

#### <a name="apidoc.element.thinky.model.prototype.docAddListener"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docAddListener (eventKey, listener)](#apidoc.element.thinky.model.prototype.docAddListener)
- description and source-code
```javascript
docAddListener = function (eventKey, listener) {
  var listeners = this._getModel()._listeners;
  if (listeners[eventKey] == null) {
    listeners[eventKey] = [];
  }
  listeners[eventKey].push({
    once: false,
    listener: listener
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docListeners"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docListeners (eventKey, raw)](#apidoc.element.thinky.model.prototype.docListeners)
- description and source-code
```javascript
docListeners = function (eventKey, raw) {
  if (eventKey == null) {
    return this._getModel()._listeners
  }

  raw = raw || true;
  if (raw === true) {
    return this._getModel()._listeners[eventKey];
  }
  else {
    return this._getModel()._listeners[eventKey].map(function(fn) {
      return fn.listener;
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docOn"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docOn (eventKey, listener)](#apidoc.element.thinky.model.prototype.docOn)
- description and source-code
```javascript
docOn = function (eventKey, listener) {
  var listeners = this._getModel()._listeners;
  if (listeners[eventKey] == null) {
    listeners[eventKey] = [];
  }
  listeners[eventKey].push({
    once: false,
    listener: listener
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docOnce"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docOnce (eventKey, listener)](#apidoc.element.thinky.model.prototype.docOnce)
- description and source-code
```javascript
docOnce = function (eventKey, listener) {
  var listeners = this._getModel()._listeners;
  if (listeners[eventKey] == null) {
    listeners[eventKey] = [];
  }
  listeners[eventKey].push({
    once: true,
    listener: listener
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docRemoveAllListeners"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docRemoveAllListeners (ev)](#apidoc.element.thinky.model.prototype.docRemoveAllListeners)
- description and source-code
```javascript
docRemoveAllListeners = function (ev) {
  if (ev === undefined) {
    delete this._getModel()._listeners[ev]
  }
  else {
    this._getModel()._listeners = {};
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docRemoveListener"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docRemoveListener (ev, listener)](#apidoc.element.thinky.model.prototype.docRemoveListener)
- description and source-code
```javascript
docRemoveListener = function (ev, listener) {
  if (Array.isArray(this._getModel()._listeners[ev])) {
    for(var i=0; i<this._getModel()._listeners[ev].length; i++) {
      if (this._getModel()._listeners[ev][i] === listener) {
        this._getModel()._listeners[ev].splice(i, 1);
        break;
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.docSetMaxListeners"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>docSetMaxListeners (n)](#apidoc.element.thinky.model.prototype.docSetMaxListeners)
- description and source-code
```javascript
docSetMaxListeners = function (n) {
  this._getModel()._maxListeners = n;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.downcase"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>downcase ()](#apidoc.element.thinky.model.prototype.downcase)
- description and source-code
```javascript
downcase = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.during"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>during ()](#apidoc.element.thinky.model.prototype.during)
- description and source-code
```javascript
during = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.ensureIndex"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ensureIndex (name, fn, opts)](#apidoc.element.thinky.model.prototype.ensureIndex)
- description and source-code
```javascript
ensureIndex = function (name, fn, opts) {
  var self = this;

  if ((opts === undefined) && (util.isPlainObject(fn))) {
    opts = fn;
    fn = undefined;
  }

  return self._createIndex(name, fn, opts)
  .catch(function(error) {
    self._getModel()._setError(error);
    throw error;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.epochTime"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>epochTime ()](#apidoc.element.thinky.model.prototype.epochTime)
- description and source-code
```javascript
epochTime = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.eq"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>eq ()](#apidoc.element.thinky.model.prototype.eq)
- description and source-code
```javascript
eq = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

  var promise = this.tableReady().then(function() {
return new Promise(function(resolve, reject) {
  return r.branch(
    r.table(tableName).indexList().contains(name),
    r.table(tableName).indexWait(name),
    r.branch(
      r.table(tableName).info()('primary_key').eq(name),
      r.table(tableName).indexWait(name),
      r.table(tableName).indexCreate(name, fn, opts).do(function() {
        return r.table(tableName).indexWait(name);
      })
    )
  )
  .run()
...
```

#### <a name="apidoc.element.thinky.model.prototype.eqJoin"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>eqJoin ()](#apidoc.element.thinky.model.prototype.eqJoin)
- description and source-code
```javascript
eqJoin = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.error"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>error ()](#apidoc.element.thinky.model.prototype.error)
- description and source-code
```javascript
error = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
      }
    });

    //TODO Remove once
    self.getModel().ready().then(function() {
      Promise.all(promises).then(function() {
        self._onSavedBelongsTo(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject);
      }).error(reject);
    });
  });
  return p;
}


/**
...
```

#### <a name="apidoc.element.thinky.model.prototype.execute"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>execute (options)](#apidoc.element.thinky.model.prototype.execute)
- description and source-code
```javascript
execute = function (options) {
  var query = new Query(this);
  return query.execute(options);
}
```
- example usage
```shell
...

Model.prototype.run = function(options) {
var query = new Query(this);
return query.run(options);
}
Model.prototype.execute = function(options) {
var query = new Query(this);
return query.execute(options);
}

Model.prototype.save = function(docs, options) {
var self = this;
var r = self._getModel()._thinky.r;
var isArray = Array.isArray(docs);
...
```

#### <a name="apidoc.element.thinky.model.prototype.expr"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>expr ()](#apidoc.element.thinky.model.prototype.expr)
- description and source-code
```javascript
expr = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

return Promise.all([self.ready(), joinedModel.ready()]);
  }
};

(function() {
  // Import rethinkdbdash methods
  var Term = require('rethinkdbdash')({pool: false}).expr(1).__proto__;
  util.loopKeys(Term, function(Term, key) {
if (!Term.hasOwnProperty(key)) return;
if (key === 'run' || key[0] === '_') return;

(function(key) {
  switch (key) {
    case 'orderBy':
...
```

#### <a name="apidoc.element.thinky.model.prototype.february"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>february ()](#apidoc.element.thinky.model.prototype.february)
- description and source-code
```javascript
february = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.fill"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>fill ()](#apidoc.element.thinky.model.prototype.fill)
- description and source-code
```javascript
fill = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.filter"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>filter ()](#apidoc.element.thinky.model.prototype.filter)
- description and source-code
```javascript
filter = function () {
  var query = new Query(this);
  if ((arguments.length === 1)
    && (util.isPlainObject(arguments[0]))) {

    // Optimize a filter with an object
    // We replace the first key that match an index name
    var filter = arguments[0];

    var keys = Object.keys(filter).sort(); // Lexicographical order
    for(var i=0 ; i<keys.length; i++) {
      var index = keys[i];

      if (this._getModel()._indexes[index] === true) { // Index found
        query = query.getAll(filter[index], {index: index});
        delete filter[index];
        break;
      }
    }
  }

  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.finally"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>finally ()](#apidoc.element.thinky.model.prototype.finally)
- description and source-code
```javascript
finally = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.floor"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>floor ()](#apidoc.element.thinky.model.prototype.floor)
- description and source-code
```javascript
floor = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.fold"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>fold ()](#apidoc.element.thinky.model.prototype.fold)
- description and source-code
```javascript
fold = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.forEach"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>forEach ()](#apidoc.element.thinky.model.prototype.forEach)
- description and source-code
```javascript
forEach = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.friday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>friday ()](#apidoc.element.thinky.model.prototype.friday)
- description and source-code
```javascript
friday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.ge"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ge ()](#apidoc.element.thinky.model.prototype.ge)
- description and source-code
```javascript
ge = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.geojson"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>geojson ()](#apidoc.element.thinky.model.prototype.geojson)
- description and source-code
```javascript
geojson = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  else if (type.isPoint(schema)) {
if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
  var keys = Object.keys(doc).sort();
  if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
    return r.point(doc.longitude, doc.latitude)
  }
  else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
    return r.geojson(doc)
  }
}
else if (Array.isArray(doc)) {
  if ((doc.length === 2) && (typeof doc[0] === "number") && (typeof doc[1] === "number")) {
    return r.point(doc[0], doc[1])
  }
}
...
```

#### <a name="apidoc.element.thinky.model.prototype.get"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>get ()](#apidoc.element.thinky.model.prototype.get)
- description and source-code
```javascript
get = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.model.prototype.getAll"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getAll ()](#apidoc.element.thinky.model.prototype.getAll)
- description and source-code
```javascript
getAll = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  // Purge the database
  var promises = [];
  util.loopKeys(self._getModel()._joins, function(joins, field) {
var join = joins[field];
var joinedModel = join.model;

if ((join.type === 'hasOne') || (join.type === 'hasMany')) {
  promises.push(r.table(joinedModel.getTableName()).getAll(self[join.leftKey], {index: join.rightKey}).replace(function(doc) {
    return doc.without(join.rightKey)
  }).run())
}
// nothing to do for "belongsTo"
else if (join.type === 'hasAndBelongsToMany') {
  if (self.getModel()._getModel()._pk === join.leftKey) {
    // [1]
...
```

#### <a name="apidoc.element.thinky.model.prototype.getField"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getField ()](#apidoc.element.thinky.model.prototype.getField)
- description and source-code
```javascript
getField = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.getIntersecting"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getIntersecting ()](#apidoc.element.thinky.model.prototype.getIntersecting)
- description and source-code
```javascript
getIntersecting = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.getJoin"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getJoin ()](#apidoc.element.thinky.model.prototype.getJoin)
- description and source-code
```javascript
getJoin = function () {
  var query = new Query(this);
  return query.getJoin.apply(query, arguments)
}
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.model.prototype.getNearest"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getNearest ()](#apidoc.element.thinky.model.prototype.getNearest)
- description and source-code
```javascript
getNearest = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.getOptions"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getOptions ()](#apidoc.element.thinky.model.prototype.getOptions)
- description and source-code
```javascript
getOptions = function () {
  return this._options;
}
```
- example usage
```shell
...
this._model = model._getModel(); // The instance of Model

// We don't want to store options if they are different
// than the one provided by the model
if (util.isPlainObject(options)) {
  this._schemaOptions = {};
  this._schemaOptions.enforce_missing =
      (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
  this._schemaOptions.enforce_extra =
      (options.enforce_extra != null) ? options.enforce_extra : model.getOptions().enforce_extra;
  this._schemaOptions.enforce_type =
      (options.enforce_type != null) ? options.enforce_type : model.getOptions().enforce_type;
}

//TODO: We do not need to make a deep copy. We can do the same as for this._schemaOptions.
...
```

#### <a name="apidoc.element.thinky.model.prototype.getTableName"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>getTableName ()](#apidoc.element.thinky.model.prototype.getTableName)
- description and source-code
```javascript
getTableName = function () {
  return this._getModel()._name;
}
```
- example usage
```shell
...
self._getModel()._schema.validate(self, prefix, schemaOptions)

if (util.isPlainObject(modelToValidate) === false) {
  modelToValidate = {};
}

var constructor = self.__proto__.constructor;
validatedModel[constructor.getTableName()] = true;

// Validate joined documents
util.loopKeys(self._getModel()._joins, function(joins, key) {
  if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
    switch (joins[key].type) {
      case 'hasOne':
      case 'belongsTo':
...
```

#### <a name="apidoc.element.thinky.model.prototype.grant"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>grant ()](#apidoc.element.thinky.model.prototype.grant)
- description and source-code
```javascript
grant = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.group"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>group ()](#apidoc.element.thinky.model.prototype.group)
- description and source-code
```javascript
group = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.gt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>gt ()](#apidoc.element.thinky.model.prototype.gt)
- description and source-code
```javascript
gt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.hasAndBelongsToMany"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasAndBelongsToMany (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasAndBelongsToMany)
- description and source-code
```javascript
hasAndBelongsToMany = function (joinedModel, fieldDoc, leftKey, rightKey, options) {
  var self = this;
  var link, query;
  var thinky = this._getModel()._thinky;
  options = options || {};

  if ((joinedModel instanceof Model) === false) {
    throw new Error("First argument of 'hasAndBelongsToMany' must be a Model")
  }
  if (fieldDoc in self._getModel()._joins) {
    throw new Error("The field '"+fieldDoc+"' is already used by another relation.");
  }
  if (fieldDoc === "_apply") {
    throw new Error("The field '_apply' is reserved by thinky. Please use another one.");
  }

  if (this._getModel()._name < joinedModel._getModel()._name) {
    link = this._getModel()._name+"_"+joinedModel._getModel()._name;
  }
  else {
    link = joinedModel._getModel()._name+"_"+this._getModel()._name;
  }
  if (typeof options.type === 'string') {
    link = link+"_"+options.type;
  }
  else if (typeof options.type !== 'undefined') {
    throw new Error('options.type should be a string or undefined.')
  }

  var linkModel;
  if (thinky.models[link] === undefined) {
    // Create a model, claim the namespace and create the table
    // passes table options to the underlying model (e.g. replicas, shards)
    linkModel = thinky.createModel(link, {}, { table: options.table });
  }
  else {
    linkModel = thinky.models[link];
  }


  this._getModel()._joins[fieldDoc] = {
    model: joinedModel,
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'hasAndBelongsToMany',
    link: link,
    linkModel: linkModel
  }

  joinedModel._getModel()._reverseJoins[self.getTableName()] = {
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'hasAndBelongsToMany',
    link: link,
    linkModel: linkModel
  }

  if (options.init !== false) {
    var r = self._getModel()._thinky.r;

    var query;
    if ((this.getTableName() === joinedModel.getTableName())
      && (leftKey === rightKey)) {
      // The relation is built for the same model, using the same key
      // Create a multi index
      query = r.branch(
        r.table(link).indexList().contains(leftKey+"_"+rightKey),
        r.table(link).indexWait(leftKey+"_"+rightKey),
        r.table(link).indexCreate(leftKey+"_"+rightKey, function(doc) {
          return doc(leftKey+"_"+rightKey)
        }, {multi: true}).do(function() {
          return r.table(link).indexWait(leftKey+"_"+rightKey)
        })
      )
    }
    else {
      query = r.branch(
        r.table(link).indexList().contains(self.getTableName()+'_'+leftKey),
        r.table(link).indexWait(self.getTableName()+'_'+leftKey),
        r.table(link).indexCreate(self.getTableName()+'_'+leftKey).do(function() {
          return r.table(link).indexWait(self.getTableName()+'_'+leftKey)
        })
      ).do(function() {
        return r.branch(
          r.table(link).indexList().contains(joinedModel.getTableName()+'_'+rightKey),
          r.table(link).indexWait(joinedModel.getTableName()+'_'+rightKey),
          r.table(link).indexCreate(joinedModel.getTableName()+'_'+rightKey).do(function() {
            return r.table(link).indexWait(joinedModel.getTableName()+'_'+rightKey)
          })
        )
      })

    }

    var linkPromise = linkModel.ready().then(function() {
      return query.run()
      .then(function() {
        self._getModel()._indexes[leftKey] = true;
        joinedModel._getModel()._indexes[rightKey] = true;
      })
      .error(function(error) {
        if (error.message.match(/^Index '/)) {
          return;
        }
        if (error.message.match(/^Table '.*' already exists/)) {
          return;
        }
        self._getModel()._setError(error);
        joinedModel._getModel()._setError(error);
        throw error;
      });
    })
    .then(function() {
      self._createIndex(leftKey)
      .catch(function(error) {
        self._getModel()._setError(error);
        joinedModel._getModel()._setError(error);
      });

      joinedModel._createIndex(rightKey)
      .catch(function(error) {
        self._getModel()._setError(error);
        joinedModel._getModel()._setError(error);
      });
    });

    joinedModel._wait ...
```
- example usage
```shell
...
    promises.push(r.table(joinedModel.getTableName()).getAll(self[join.rightKey], {index: join.leftKey}).replace(function(doc) {
      return doc.without(join.leftKey)
    }).run())
  }
  // nothing to do for "belongsTo"
  else if (join.type === 'hasAndBelongsToMany') {
    // Purge only if the key is a primary key
    // What was called is joinedModel.hasAndBelongsToMany(self, fieldDoc, leftKey, rightKey)
    if (self.getModel()._getModel()._pk === join.leftKey) {
      promises.push(r.table(join.link).getAll(self[join.rightKey], {index: self.getModel().getTableName()+"_"+join.rightKey}).delete
().run())
    }
  }
});

// Delete itself
...
```

#### <a name="apidoc.element.thinky.model.prototype.hasFields"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasFields ()](#apidoc.element.thinky.model.prototype.hasFields)
- description and source-code
```javascript
hasFields = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
...
```

#### <a name="apidoc.element.thinky.model.prototype.hasMany"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasMany (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasMany)
- description and source-code
```javascript
hasMany = function (joinedModel, fieldDoc, leftKey, rightKey, options) {
  var self  = this;

  if ((joinedModel instanceof Model) === false) {
    throw new Error("First argument of 'hasMany' must be a Model")
  }
  if (fieldDoc in self._getModel()._joins) {
    throw new Error("The field '"+fieldDoc+"' is already used by another relation.");
  }
  if (fieldDoc === "_apply") {
    throw new Error("The field '_apply' is reserved by thinky. Please use another one.");
  }

  this._getModel()._joins[fieldDoc] = {
    model: joinedModel,
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'hasMany'
  };
  joinedModel._getModel()._localKeys[rightKey] = true;

  options = options || {};
  if (options.init !== false) {
    var newIndex = joinedModel._createIndex(rightKey)
    .catch(function(error) {
      self._getModel()._setError(error);
      joinedModel._getModel()._setError(error);
    });
    self._waitFor(newIndex);
  }
}
```
- example usage
```shell
...
/*
 * joinedModel: the joined model
 * fieldDoc: the field where the joined document will be kept
 * leftKey: the key in the model used for the join
 * rightKey: the key in the joined model used for the join
 *
 * A post has one author, and an author can write multiple posts
 * Author.hasMany(Post, "posts", "id", "authorId"
 *                 ^- author.id
 */
Model.prototype.hasMany = function(joinedModel, fieldDoc, leftKey, rightKey, options) {
var self  = this;

if ((joinedModel instanceof Model) === false) {
  throw new Error("First argument of 'hasMany' must be a Model")
...
```

#### <a name="apidoc.element.thinky.model.prototype.hasOne"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hasOne (joinedModel, fieldDoc, leftKey, rightKey, options)](#apidoc.element.thinky.model.prototype.hasOne)
- description and source-code
```javascript
hasOne = function (joinedModel, fieldDoc, leftKey, rightKey, options) {
  var self  = this;

  if ((joinedModel instanceof Model) === false) {
    throw new Error("First argument of 'hasOne' must be a Model")
  }
  if (fieldDoc in self._getModel()._joins) {
    throw new Error("The field '"+fieldDoc+"' is already used by another relation.");
  }
  if (fieldDoc === "_apply") {
    throw new Error("The field '_apply' is reserved by thinky. Please use another one.");
  }
  self._getModel()._joins[fieldDoc] = {
    model: joinedModel,
    leftKey: leftKey,
    rightKey: rightKey,
    type: 'hasOne'
  }
  joinedModel._getModel()._localKeys[rightKey] = true;

  options = options || {};
  if (options.init !== false) {
    var newIndex = joinedModel._createIndex(rightKey)
    .catch(function(error) {
      joinedModel._getModel()._setError(error);
      self._getModel()._setError(error);
    });
    self._waitFor(newIndex);
  }
}
```
- example usage
```shell
...
* joinedModel: the joined model
* fieldDoc: the field where the joined document will be kept
* leftKey: the key in the model used for the join
* rightKey: the key in the joined model used for the join
*
* The foreign key is stores in the joinedModel
*
* Post.hasOne(Author, "author", "id", "postId"
*                ^- post.id
*
* options can be:
* - init: Boolean (create an index or not)
* - timeFormat: 'raw'/'native'
* - enforce_extra: 'strict'/'remove'/'none'
* - enforce_missing: Boolean
...
```

#### <a name="apidoc.element.thinky.model.prototype.hours"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>hours ()](#apidoc.element.thinky.model.prototype.hours)
- description and source-code
```javascript
hours = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.http"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>http ()](#apidoc.element.thinky.model.prototype.http)
- description and source-code
```javascript
http = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.inTimezone"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>inTimezone ()](#apidoc.element.thinky.model.prototype.inTimezone)
- description and source-code
```javascript
inTimezone = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.includes"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>includes ()](#apidoc.element.thinky.model.prototype.includes)
- description and source-code
```javascript
includes = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.indexCreate"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexCreate ()](#apidoc.element.thinky.model.prototype.indexCreate)
- description and source-code
```javascript
indexCreate = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
    return new Promise(function(resolve, reject) {
return r.branch(
  r.table(tableName).indexList().contains(name),
  r.table(tableName).indexWait(name),
  r.branch(
    r.table(tableName).info()('primary_key').eq(name),
    r.table(tableName).indexWait(name),
    r.table(tableName).indexCreate(name, fn, opts).do(function() {
      return r.table(tableName).indexWait(name);
    })
  )
)
.run()
.then(resolve)
.error(function(error) {
...
```

#### <a name="apidoc.element.thinky.model.prototype.indexDrop"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexDrop ()](#apidoc.element.thinky.model.prototype.indexDrop)
- description and source-code
```javascript
indexDrop = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.indexList"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexList ()](#apidoc.element.thinky.model.prototype.indexList)
- description and source-code
```javascript
indexList = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
...
```

#### <a name="apidoc.element.thinky.model.prototype.indexRename"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexRename ()](#apidoc.element.thinky.model.prototype.indexRename)
- description and source-code
```javascript
indexRename = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.indexStatus"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexStatus ()](#apidoc.element.thinky.model.prototype.indexStatus)
- description and source-code
```javascript
indexStatus = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.indexWait"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexWait ()](#apidoc.element.thinky.model.prototype.indexWait)
- description and source-code
```javascript
indexWait = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
      )
...
```

#### <a name="apidoc.element.thinky.model.prototype.indexesOf"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>indexesOf ()](#apidoc.element.thinky.model.prototype.indexesOf)
- description and source-code
```javascript
indexesOf = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.info"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>info ()](#apidoc.element.thinky.model.prototype.info)
- description and source-code
```javascript
info = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

  var promise = this.tableReady().then(function() {
return new Promise(function(resolve, reject) {
  return r.branch(
    r.table(tableName).indexList().contains(name),
    r.table(tableName).indexWait(name),
    r.branch(
      r.table(tableName).info()('primary_key').eq(name),
      r.table(tableName).indexWait(name),
      r.table(tableName).indexCreate(name, fn, opts).do(function() {
        return r.table(tableName).indexWait(name);
      })
    )
  )
  .run()
...
```

#### <a name="apidoc.element.thinky.model.prototype.innerJoin"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>innerJoin ()](#apidoc.element.thinky.model.prototype.innerJoin)
- description and source-code
```javascript
innerJoin = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.insert"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>insert ()](#apidoc.element.thinky.model.prototype.insert)
- description and source-code
```javascript
insert = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

var querySaveSelf; // The query to save the document on which 'save'/'saveAll' was called.
// We haven't validated the document yet, so building the query with 'copy'
// may throw an error (for example if a Date has not a valid time).
var buildQuery = function () {
  if (self.__proto__._saved === false) {
    return querySaveSelf = r.table(constructor.getTableName())
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
      .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
...
```

#### <a name="apidoc.element.thinky.model.prototype.insertAt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>insertAt ()](#apidoc.element.thinky.model.prototype.insertAt)
- description and source-code
```javascript
insertAt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.intersects"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>intersects ()](#apidoc.element.thinky.model.prototype.intersects)
- description and source-code
```javascript
intersects = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>isEmpty ()](#apidoc.element.thinky.model.prototype.isEmpty)
- description and source-code
```javascript
isEmpty = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.january"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>january ()](#apidoc.element.thinky.model.prototype.january)
- description and source-code
```javascript
january = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.js"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>js ()](#apidoc.element.thinky.model.prototype.js)
- description and source-code
```javascript
js = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.json"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>json ()](#apidoc.element.thinky.model.prototype.json)
- description and source-code
```javascript
json = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.july"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>july ()](#apidoc.element.thinky.model.prototype.july)
- description and source-code
```javascript
july = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.june"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>june ()](#apidoc.element.thinky.model.prototype.june)
- description and source-code
```javascript
june = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.keys"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>keys ()](#apidoc.element.thinky.model.prototype.keys)
- description and source-code
```javascript
keys = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
      doc = numericDate;
    }
  }
  return new Date(doc); // Use r.ISO8601 and not 'new Date()' to keep timezone
}
else if (type.isPoint(schema)) {
  if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
    var keys = Object.keys(doc).sort();
    if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
      return r.point(doc.longitude, doc.latitude)
    }
    else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
      return r.geojson(doc)
    }
  }
...
```

#### <a name="apidoc.element.thinky.model.prototype.le"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>le ()](#apidoc.element.thinky.model.prototype.le)
- description and source-code
```javascript
le = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.limit"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>limit ()](#apidoc.element.thinky.model.prototype.limit)
- description and source-code
```javascript
limit = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.line"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>line ()](#apidoc.element.thinky.model.prototype.line)
- description and source-code
```javascript
line = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.literal"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>literal ()](#apidoc.element.thinky.model.prototype.literal)
- description and source-code
```javascript
literal = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.lt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>lt ()](#apidoc.element.thinky.model.prototype.lt)
- description and source-code
```javascript
lt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
}

if ((model.getTableName() === joinedModel.getTableName())
    && (joins[field].leftKey === joins[field].rightKey)) {
  linkValue = self._query(joins[field].leftKey).do(function(leftKey) {
    return link.do(function(rightKey) {
      return r.branch(
          rightKey.lt(leftKey),
          r.object(
            'id', rightKey.add('_').add(leftKey),
            joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
          ),
          r.object(
            'id', leftKey.add('_').add(rightKey),
            joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
...
```

#### <a name="apidoc.element.thinky.model.prototype.map"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>map ()](#apidoc.element.thinky.model.prototype.map)
- description and source-code
```javascript
map = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
}

raw = raw || true;
if (raw === true) {
  return this._getModel()._listeners[eventKey];
}
else {
  return this._getModel()._listeners[eventKey].map(function(fn) {
    return fn.listener;
  });
}
}

Model.prototype.docSetMaxListeners = function(n) {
this._getModel()._maxListeners = n;
...
```

#### <a name="apidoc.element.thinky.model.prototype.march"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>march ()](#apidoc.element.thinky.model.prototype.march)
- description and source-code
```javascript
march = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.match"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>match ()](#apidoc.element.thinky.model.prototype.match)
- description and source-code
```javascript
match = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

/**
 * Creates an appropriate error given either an instance of Error or a message
 * from the RethinkDB driver
 */
errors.create = function(errorOrMessage) {
var message = (errorOrMessage instanceof Error) ? errorOrMessage.message : errorOrMessage;
if (message.match(errors.DOCUMENT_NOT_FOUND_REGEX)) {
  return new errors.DocumentNotFound(message);
} else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
  var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
  return new errors.DuplicatePrimaryKey(message, primaryKey);
} else if (errorOrMessage instanceof Error) {
  return errorOrMessage;
}
...
```

#### <a name="apidoc.element.thinky.model.prototype.max"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>max ()](#apidoc.element.thinky.model.prototype.max)
- description and source-code
```javascript
max = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
options = util.mergeOptions(options, schema.options);
var result;
switch(schema._type) {
  case String:
    result = type.string().options(options).validator(schema.validator).enum(schema.enum);
    if (schema.default !== undefined) { result.default(schema.default); }
    if (typeof schema.min === "number") { result.min(schema.min); }
    if (typeof schema.max === "number") { result.max(schema.max); }
    if (typeof schema.length === "number") { result.length(schema.length); }
    if (schema.alphanum === true) { result.alphanum(); }
    if (schema.lowercase === true) { result.lowercase(); }
    if (schema.uppercase === true) { result.uppercase(); }
    if (typeof schema.regex === "string") { result.regex(regex, schema.flags); }
    return result;
  case Number:
...
```

#### <a name="apidoc.element.thinky.model.prototype.maxval"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>maxval ()](#apidoc.element.thinky.model.prototype.maxval)
- description and source-code
```javascript
maxval = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.may"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>may ()](#apidoc.element.thinky.model.prototype.may)
- description and source-code
```javascript
may = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.merge"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>merge ()](#apidoc.element.thinky.model.prototype.merge)
- description and source-code
```javascript
merge = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  gotModel[model.getTableName()] = true;

  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
...
```

#### <a name="apidoc.element.thinky.model.prototype.min"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>min ()](#apidoc.element.thinky.model.prototype.min)
- description and source-code
```javascript
min = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  content: String,
  idAuthor: String
});

// You can also add constraints on the schema
var Author = thinky.createModel("Author", {
  id: type.string(),      // a normal string
  name: type.string().min(2),  // a string of at least two characters
  email: type.string().email()  // a string that is a valid email
});

// Join the models
Post.belongsTo(Author, "author", "idAuthor", "id");
'''
...
```

#### <a name="apidoc.element.thinky.model.prototype.minutes"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>minutes ()](#apidoc.element.thinky.model.prototype.minutes)
- description and source-code
```javascript
minutes = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.minval"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>minval ()](#apidoc.element.thinky.model.prototype.minval)
- description and source-code
```javascript
minval = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.mod"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>mod ()](#apidoc.element.thinky.model.prototype.mod)
- description and source-code
```javascript
mod = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.monday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>monday ()](#apidoc.element.thinky.model.prototype.monday)
- description and source-code
```javascript
monday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.month"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>month ()](#apidoc.element.thinky.model.prototype.month)
- description and source-code
```javascript
month = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.mul"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>mul ()](#apidoc.element.thinky.model.prototype.mul)
- description and source-code
```javascript
mul = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.ne"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ne ()](#apidoc.element.thinky.model.prototype.ne)
- description and source-code
```javascript
ne = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.not"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>not ()](#apidoc.element.thinky.model.prototype.not)
- description and source-code
```javascript
not = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.november"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>november ()](#apidoc.element.thinky.model.prototype.november)
- description and source-code
```javascript
november = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.now"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>now ()](#apidoc.element.thinky.model.prototype.now)
- description and source-code
```javascript
now = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.nth"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>nth ()](#apidoc.element.thinky.model.prototype.nth)
- description and source-code
```javascript
nth = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
  result.count().eq(1),
...
```

#### <a name="apidoc.element.thinky.model.prototype.object"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>object ()](#apidoc.element.thinky.model.prototype.object)
- description and source-code
```javascript
object = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...

  if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
    innerQuery = modelToGet[key]._apply(innerQuery);
  }
  innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
  return r.branch(
    result.count().eq(1),
    r.object(key, innerQuery),
    r.branch(
      result.count().eq(0),
      {},
      r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
    )
  )
}),
...
```

#### <a name="apidoc.element.thinky.model.prototype.october"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>october ()](#apidoc.element.thinky.model.prototype.october)
- description and source-code
```javascript
october = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.offsetsOf"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>offsetsOf ()](#apidoc.element.thinky.model.prototype.offsetsOf)
- description and source-code
```javascript
offsetsOf = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.or"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>or ()](#apidoc.element.thinky.model.prototype.or)
- description and source-code
```javascript
or = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.orderBy"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>orderBy ()](#apidoc.element.thinky.model.prototype.orderBy)
- description and source-code
```javascript
orderBy = function () {
  var query = new Query(this);
  if ((arguments.length === 1)
    && (typeof arguments[0] === 'string')
    && (this._getModel()._indexes[arguments[0]] === true)) {

      query = query[key]({index: arguments[0]});
      return query;
  }
  else {
    query = query[key].apply(query, arguments);
    return query;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.outerJoin"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>outerJoin ()](#apidoc.element.thinky.model.prototype.outerJoin)
- description and source-code
```javascript
outerJoin = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.pluck"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>pluck ()](#apidoc.element.thinky.model.prototype.pluck)
- description and source-code
```javascript
pluck = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.point"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>point ()](#apidoc.element.thinky.model.prototype.point)
- description and source-code
```javascript
point = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  }
  return new Date(doc); // Use r.ISO8601 and not 'new Date()' to keep timezone
}
else if (type.isPoint(schema)) {
  if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
    var keys = Object.keys(doc).sort();
    if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
      return r.point(doc.longitude, doc.latitude)
    }
    else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
      return r.geojson(doc)
    }
  }
  else if (Array.isArray(doc)) {
    if ((doc.length === 2) && (typeof doc[0] === "number") && (typeof doc[1] === "number")) {
...
```

#### <a name="apidoc.element.thinky.model.prototype.polygon"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>polygon ()](#apidoc.element.thinky.model.prototype.polygon)
- description and source-code
```javascript
polygon = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.polygonSub"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>polygonSub ()](#apidoc.element.thinky.model.prototype.polygonSub)
- description and source-code
```javascript
polygonSub = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.post"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>post (ev, fn)](#apidoc.element.thinky.model.prototype.post)
- description and source-code
```javascript
post = function (ev, fn) {
  if (typeof fn !== "function") {
    throw new Error("Second argument to 'pre' must be a function");
  }
  if (fn.length > 1) {
    throw new Error("Second argument to 'pre' must be a function with at most one argument.");
  }
  if (Array.isArray(this._post[ev]) === false) {
    throw new Error("No post-hook available for the event '"+ev+"'.")
  }
  this._getModel()._async[ev] = this._getModel()._async[ev] || (fn.length === 1)
  this._getModel()._post[ev].push(fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.pre"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>pre (ev, fn)](#apidoc.element.thinky.model.prototype.pre)
- description and source-code
```javascript
pre = function (ev, fn) {
  if (typeof fn !== "function") {
    throw new Error("Second argument to 'pre' must be a function");
  }
  if (fn.length > 1) {
    throw new Error("Second argument to 'pre' must be a function with at most one argument.");
  }
  if (Array.isArray(this._pre[ev]) === false) {
    throw new Error("No pre-hook available for the event '"+ev+"'.")
  }
  this._getModel()._async[ev] = this._getModel()._async[ev] || (fn.length === 1)
  this._getModel()._pre[ev].push(fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.prepend"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>prepend ()](#apidoc.element.thinky.model.prototype.prepend)
- description and source-code
```javascript
prepend = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.random"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>random ()](#apidoc.element.thinky.model.prototype.random)
- description and source-code
```javascript
random = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.range"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>range ()](#apidoc.element.thinky.model.prototype.range)
- description and source-code
```javascript
range = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.ready"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ready ()](#apidoc.element.thinky.model.prototype.ready)
- description and source-code
```javascript
ready = function () {
  var requirements = [];

  // Ensure the Model's table is ready
  requirements.push(this.tableReady());

  // Ensure all other pending promises have been resolved
  requirements.push(this._promisesReady());

  return Promise.all(requirements);
}
```
- example usage
```shell
...
 * @param {Function} executeInsert the method that will execute the batch insert
 * @return {Promise}
 */
Document.prototype._batchSaveSelf = function(executeInsert) {
  var self = this;

  return new Promise(function(resolve, reject) {
    self.getModel().ready().then(function() {
      executeInsert(resolve, reject)
    });
  })
}


/**
...
```

#### <a name="apidoc.element.thinky.model.prototype.rebalance"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>rebalance ()](#apidoc.element.thinky.model.prototype.rebalance)
- description and source-code
```javascript
rebalance = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.reconfigure"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>reconfigure ()](#apidoc.element.thinky.model.prototype.reconfigure)
- description and source-code
```javascript
reconfigure = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.reduce"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>reduce ()](#apidoc.element.thinky.model.prototype.reduce)
- description and source-code
```javascript
reduce = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.removeRelations"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>removeRelations (relationsToRemove)](#apidoc.element.thinky.model.prototype.removeRelations)
- description and source-code
```javascript
removeRelations = function (relationsToRemove) {
  var query = new Query(this);
  return query.removeRelations(relationsToRemove);
}
```
- example usage
```shell
...
Model.prototype.getJoin = function() {
  var query = new Query(this);
  return query.getJoin.apply(query, arguments)
}

Model.prototype.removeRelations = function(relationsToRemove) {
  var query = new Query(this);
  return query.removeRelations(relationsToRemove);
}


Model.prototype.run = function(options) {
  var query = new Query(this);
  return query.run(options);
}
...
```

#### <a name="apidoc.element.thinky.model.prototype.replace"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>replace ()](#apidoc.element.thinky.model.prototype.replace)
- description and source-code
```javascript
replace = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
      .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
  }
}

self.getModel().ready().then(function() {
  util.tryCatch(function() {
    // Validate the document before saving it
    var promise = self.validate();
...
```

#### <a name="apidoc.element.thinky.model.prototype.round"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>round ()](#apidoc.element.thinky.model.prototype.round)
- description and source-code
```javascript
round = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.row"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>row ()](#apidoc.element.thinky.model.prototype.row)
- description and source-code
```javascript
row = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.run"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>run (options)](#apidoc.element.thinky.model.prototype.run)
- description and source-code
```javascript
run = function (options) {
  var query = new Query(this);
  return query.run(options);
}
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.model.prototype.sample"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sample ()](#apidoc.element.thinky.model.prototype.sample)
- description and source-code
```javascript
sample = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.saturday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>saturday ()](#apidoc.element.thinky.model.prototype.saturday)
- description and source-code
```javascript
saturday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.save"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>save (docs, options)](#apidoc.element.thinky.model.prototype.save)
- description and source-code
```javascript
save = function (docs, options) {
  var self = this;
  var r = self._getModel()._thinky.r;
  var isArray = Array.isArray(docs);

  if (!isArray) {
    docs = [docs];
  }

  var p = new Promise(function(mainResolve, mainReject) {
    var toSave = docs.length;

    var resolves = [];
    var rejects = [];
    var executeInsert = function (resolve, reject) {
      toSave--;
      resolves.push(resolve);
      rejects.push(reject);

      if (toSave === 0) {
        var copies = [];
        for(var i=0; i<docs.length; i++) {
          copies.push(docs[i]._makeSavableCopy());
        }
        var _options;
        if (util.isPlainObject(options)) {
          _options = util.deepCopy(options);
        }
        else {
          _options = {};
        }
        _options.returnChanges = 'always';
        r.table(self.getTableName()).insert(copies, _options).run().then(function(results) {
          if (results.errors === 0) {
            // results.changes currently does not enforce the same order as docs
            if (Array.isArray(results.changes)) {
              for(var i=0; i<results.changes.length; i++) {
                docs[i]._merge(results.changes[i].new_val);
                if (docs[i]._getModel().needToGenerateFields === true) {
                  docs[i]._generateDefault();
                }
                docs[i]._setOldValue(util.deepCopy(results.changes[i].old_val));
                docs[i].setSaved();
                docs[i].emit('saved', docs[i]);
              }
            }
            for(i=0; i<resolves.length; i++) {
              resolves[i]();
            }
          }
          else {
            //TODO Expand error with more information
            for(var i=0; i<rejects.length; i++) {
              rejects[i](new Error("An error occurred during the batch insert. Original results:\n"+JSON.stringify(results, null
, 2)));
            }
          }
        }).error(reject);
      }
    };

    var promises = [];
    var foundNonValidDoc = false;
    for(var i=0; i<docs.length; i++) {
      if (foundNonValidDoc === true) {
        return;
      }
      if (docs[i] instanceof Document === false) {
        docs[i] = new self(docs[i]);
      }
      var promise;
      util.tryCatch(function() {
        promise = docs[i].validate();
        if (promise instanceof Promise) {
          promises.push(promise)
        }
      }, function(error) {
        foundNonValidDoc = true;
        mainReject(new Errors.ValidationError("One of the documents is not valid. Original error:\n"+error.message))
      });
    }

    if (foundNonValidDoc === false) {
      Promise.all(promises).then(function() {
        var promises = [];
        for(var i=0; i<docs.length; i++) {
          promises.push(docs[i]._batchSave(executeInsert));
        }
        Promise.all(promises).then(function() {
          mainResolve(docs);
        }).error(function(error) {
          mainReject(error)
        });
      }).error(function(error) {
        mainReject(new Errors.ValidationError("One of the documents is not valid. Original error:\n"+error.message))
      });
    }
  })

  if (!isArray) {
    return p.get(0);
  }

  return p;
}
```
- example usage
```shell
...
        }).error(reject);
      }))
    })(key);
  }
  else if ((deleteSelf === true) && (deletedDocs.indexOf(self[key]) === -1)) {
    delete self[key][joins[key].rightKey];
    if (self[key].isSaved() === true) {
      promises.push(self[key].save({}, false, {}, true, false));
    }
  }
}
if ((joins[key].type === 'belongsTo') && (self[key] instanceof Document)) {
  if ((self[key].isSaved() === true) &&
    ((key in docToDelete) || ((deleteAll === true) && (deletedDocs.indexOf(self[key]) === -1)))) {
...
```

#### <a name="apidoc.element.thinky.model.prototype.seconds"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>seconds ()](#apidoc.element.thinky.model.prototype.seconds)
- description and source-code
```javascript
seconds = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.september"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>september ()](#apidoc.element.thinky.model.prototype.september)
- description and source-code
```javascript
september = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.setDifference"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setDifference ()](#apidoc.element.thinky.model.prototype.setDifference)
- description and source-code
```javascript
setDifference = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.setInsert"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setInsert ()](#apidoc.element.thinky.model.prototype.setInsert)
- description and source-code
```javascript
setInsert = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.setIntersection"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setIntersection ()](#apidoc.element.thinky.model.prototype.setIntersection)
- description and source-code
```javascript
setIntersection = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.setUnion"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>setUnion ()](#apidoc.element.thinky.model.prototype.setUnion)
- description and source-code
```javascript
setUnion = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.skip"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>skip ()](#apidoc.element.thinky.model.prototype.skip)
- description and source-code
```javascript
skip = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.slice"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>slice ()](#apidoc.element.thinky.model.prototype.slice)
- description and source-code
```javascript
slice = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
    return;
  }
  else {
    for(var k=0; k<field.length; k++) {
      if (virtual != null) {
        virtualValue = virtual[k];
      }
      generateVirtual(field[k], {path: defaultField.path.slice(j+1), value: defaultField.value}, this, virtualValue);
    }
  }
  keepGoing = false;
}
else {
  // field cannot be undefined (doc is not undefined on the first iteration, and we'll return if it becomes undefined
  field = field[path[j]];
...
```

#### <a name="apidoc.element.thinky.model.prototype.spliceAt"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>spliceAt ()](#apidoc.element.thinky.model.prototype.spliceAt)
- description and source-code
```javascript
spliceAt = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.split"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>split ()](#apidoc.element.thinky.model.prototype.split)
- description and source-code
```javascript
split = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.status"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>status ()](#apidoc.element.thinky.model.prototype.status)
- description and source-code
```javascript
status = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.sub"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sub ()](#apidoc.element.thinky.model.prototype.sub)
- description and source-code
```javascript
sub = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.sum"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sum ()](#apidoc.element.thinky.model.prototype.sum)
- description and source-code
```javascript
sum = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.sunday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sunday ()](#apidoc.element.thinky.model.prototype.sunday)
- description and source-code
```javascript
sunday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.sync"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>sync ()](#apidoc.element.thinky.model.prototype.sync)
- description and source-code
```javascript
sync = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.table"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>table ()](#apidoc.element.thinky.model.prototype.table)
- description and source-code
```javascript
table = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
});

var querySaveSelf; // The query to save the document on which 'save'/'saveAll' was called.
// We haven't validated the document yet, so building the query with 'copy'
// may throw an error (for example if a Date has not a valid time).
var buildQuery = function () {
  if (self.__proto__._saved === false) {
    return querySaveSelf = r.table(constructor.getTableName())
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
...
```

#### <a name="apidoc.element.thinky.model.prototype.tableCreate"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableCreate ()](#apidoc.element.thinky.model.prototype.tableCreate)
- description and source-code
```javascript
tableCreate = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
if (!this._initModel) return Promise.resolve();
if (this._tableReadyPromise) return this._tableReadyPromise;

// Create the table, or push the table name in the queue.
var r = model._thinky.r;
this._tableReadyPromise = model._thinky.dbReady()
.then(function() {
  return r.tableCreate(model._name, model._table).run();
})
.error(function(error) {
  if (error.message.match(/Table '.*' already exists/)) {
    return;
  }
  model._error = error;
  // Should we throw here?
...
```

#### <a name="apidoc.element.thinky.model.prototype.tableDrop"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableDrop ()](#apidoc.element.thinky.model.prototype.tableDrop)
- description and source-code
```javascript
tableDrop = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.tableList"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableList ()](#apidoc.element.thinky.model.prototype.tableList)
- description and source-code
```javascript
tableList = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.tableReady"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tableReady ()](#apidoc.element.thinky.model.prototype.tableReady)
- description and source-code
```javascript
tableReady = function () {
  var self = this;
  var model = this._getModel();
  if (!this._initModel) return Promise.resolve();
  if (this._tableReadyPromise) return this._tableReadyPromise;

  // Create the table, or push the table name in the queue.
  var r = model._thinky.r;
  this._tableReadyPromise = model._thinky.dbReady()
  .then(function() {
    return r.tableCreate(model._name, model._table).run();
  })
  .error(function(error) {
    if (error.message.match(/Table '.*' already exists/)) {
      return;
    }
    model._error = error;
    // Should we throw here?
  });

  return this._tableReadyPromise.then(function() {
    self.emit('created');
    if (!self._pendingPromises.length) {
      self.emit('ready');
    }
  });
}
```
- example usage
```shell
...
  return doc;
}

model.__proto__ = proto;

if (options.init !== false) {
  // Setup the model's table.
  model.tableReady().then();
}
else {
  // We do not initialize the table and suppose that it already exists and
  // is ready.
  model.emit('created');
  model.emit('ready');
}
...
```

#### <a name="apidoc.element.thinky.model.prototype.then"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>then ()](#apidoc.element.thinky.model.prototype.then)
- description and source-code
```javascript
then = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
email: "orphee@gmail.com"
});

// Join the documents
post.author = author;


post.saveAll().then(function(result) {
/*
post = result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.model.prototype.thursday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>thursday ()](#apidoc.element.thinky.model.prototype.thursday)
- description and source-code
```javascript
thursday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.time"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>time ()](#apidoc.element.thinky.model.prototype.time)
- description and source-code
```javascript
time = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.timeOfDay"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>timeOfDay ()](#apidoc.element.thinky.model.prototype.timeOfDay)
- description and source-code
```javascript
timeOfDay = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.timezone"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>timezone ()](#apidoc.element.thinky.model.prototype.timezone)
- description and source-code
```javascript
timezone = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toEpochTime"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toEpochTime ()](#apidoc.element.thinky.model.prototype.toEpochTime)
- description and source-code
```javascript
toEpochTime = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toGeojson"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toGeojson ()](#apidoc.element.thinky.model.prototype.toGeojson)
- description and source-code
```javascript
toGeojson = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toISO8601"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toISO8601 ()](#apidoc.element.thinky.model.prototype.toISO8601)
- description and source-code
```javascript
toISO8601 = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toJSON ()](#apidoc.element.thinky.model.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toJsonString"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toJsonString ()](#apidoc.element.thinky.model.prototype.toJsonString)
- description and source-code
```javascript
toJsonString = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toStream"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toStream ()](#apidoc.element.thinky.model.prototype.toStream)
- description and source-code
```javascript
toStream = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.toString"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>toString ()](#apidoc.element.thinky.model.prototype.toString)
- description and source-code
```javascript
toString = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
}

/**
 * Convert the query to its string representation.
 * @return {string}
 */
Query.prototype.toString = function() {
  return this._query.toString();
}

module.exports = Query;
...
```

#### <a name="apidoc.element.thinky.model.prototype.tuesday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>tuesday ()](#apidoc.element.thinky.model.prototype.tuesday)
- description and source-code
```javascript
tuesday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.typeOf"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>typeOf ()](#apidoc.element.thinky.model.prototype.typeOf)
- description and source-code
```javascript
typeOf = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.ungroup"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>ungroup ()](#apidoc.element.thinky.model.prototype.ungroup)
- description and source-code
```javascript
ungroup = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.union"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>union ()](#apidoc.element.thinky.model.prototype.union)
- description and source-code
```javascript
union = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.upcase"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>upcase ()](#apidoc.element.thinky.model.prototype.upcase)
- description and source-code
```javascript
upcase = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.update"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>update ()](#apidoc.element.thinky.model.prototype.update)
- description and source-code
```javascript
update = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  if (joinedDocument[joinedModel._pk] === undefined) {
    return new Query(model, self, {},
        new Error('Primary key for the joined document not found for a 'hasOne/hasMany' relation.')
    );
  }
  var updateValue = {};
  updateValue[joins[field].rightKey] = self._query(joins[field].leftKey);
  return joinedModel.get(joinedDocument[joinedModel._pk]).update(updateValue, {nonAtomic: true}).run()
case 'belongsTo':
  var updateValue = {};
  if (joinedDocument[joins[field].rightKey] === undefined) {
    if (joinedDocument[joinedModel._pk] === undefined) {
      return new Query(model, self, {},
          new Error('The primary key or the joined key must be defined in the joined document for a 'belongsTo' relation.')
      );
...
```

#### <a name="apidoc.element.thinky.model.prototype.uuid"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>uuid ()](#apidoc.element.thinky.model.prototype.uuid)
- description and source-code
```javascript
uuid = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.values"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>values ()](#apidoc.element.thinky.model.prototype.values)
- description and source-code
```javascript
values = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.wait"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>wait ()](#apidoc.element.thinky.model.prototype.wait)
- description and source-code
```javascript
wait = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.wednesday"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>wednesday ()](#apidoc.element.thinky.model.prototype.wednesday)
- description and source-code
```javascript
wednesday = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.withFields"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>withFields ()](#apidoc.element.thinky.model.prototype.withFields)
- description and source-code
```javascript
withFields = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.without"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>without ()](#apidoc.element.thinky.model.prototype.without)
- description and source-code
```javascript
without = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
...
  var promises = [];
  util.loopKeys(self._getModel()._joins, function(joins, field) {
var join = joins[field];
var joinedModel = join.model;

if ((join.type === 'hasOne') || (join.type === 'hasMany')) {
  promises.push(r.table(joinedModel.getTableName()).getAll(self[join.leftKey], {index: join.rightKey}).replace(function(doc) {
    return doc.without(join.rightKey)
  }).run())
}
// nothing to do for "belongsTo"
else if (join.type === 'hasAndBelongsToMany') {
  if (self.getModel()._getModel()._pk === join.leftKey) {
    // [1]
    promises.push(r.table(join.link).getAll(self[join.leftKey], {index: self.getModel().getTableName()+"_"+join.leftKey}).delete
().run())
...
```

#### <a name="apidoc.element.thinky.model.prototype.year"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>year ()](#apidoc.element.thinky.model.prototype.year)
- description and source-code
```javascript
year = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.model.prototype.zip"></a>[function <span class="apidocSignatureSpan">thinky.model.prototype.</span>zip ()](#apidoc.element.thinky.model.prototype.zip)
- description and source-code
```javascript
zip = function () {
  var query = new Query(this);
  query = query[key].apply(query, arguments);
  return query;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.query"></a>[module thinky.query](#apidoc.module.thinky.query)

#### <a name="apidoc.element.thinky.query.query"></a>[function <span class="apidocSignatureSpan">thinky.</span>query (model, query, options, error)](#apidoc.element.thinky.query.query)
- description and source-code
```javascript
function Query(model, query, options, error) {
  var self = this;

  this._model = model; // constructor of the model we should use for the results.
  if (model !== undefined) {
    this._r = model._getModel()._thinky.r;
    util.loopKeys(model._getModel()._staticMethods, function(staticMethods, key) {
      (function(_key) {
        self[_key] = function() {
          return staticMethods[_key].apply(self, arguments);
        };
      })(key);
    });
  }

  if (query !== undefined) {
    this._query = query;
   }
  else if (model !== undefined) {
    // By default, we initialize the query to 'r.table(<tableName>)'.
    this._query = this._r.table(model.getTableName());
  }

  if (util.isPlainObject(options)) {
    if (options.postValidation) {
      this._postValidation = options.postValidation === true;
    }
    if (options.ungroup) {
      this._ungroup = options.ungroup === true;
    }
    else {
      this._ungroup = false;
    }
  }
  else { // let the user rework the result after ungroup
    this._ungroup = false;
  }
  if (error) {
    // Note 'Query.prototype.error' is defined because of 'r.error', so we shouldn't
    // defined this.error.
    this._error = error;
  }
  this._pointWrite = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.query.prototype"></a>[module thinky.query.prototype](#apidoc.module.thinky.query.prototype)

#### <a name="apidoc.element.thinky.query.prototype.ISO8601"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ISO8601 ()](#apidoc.element.thinky.query.prototype.ISO8601)
- description and source-code
```javascript
ISO8601 = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype._convertGroupedData"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_convertGroupedData (data)](#apidoc.element.thinky.query.prototype._convertGroupedData)
- description and source-code
```javascript
_convertGroupedData = function (data) {
  if (util.isPlainObject(data) && (data.$reql_type$ === "GROUPED_DATA")) {
    var result = [];
    var reduction;
    for(var i=0; i<data.data.length; i++) {
      result.push({
        group: data.data[i][0],
        reduction: data.data[i][1]
      });
    }
    return result;
  }
  else {
    return data;
  }
}
```
- example usage
```shell
...
    }

    if (parse === true) {
      return self._model._parse(result, self._ungroup);
    }

    if (groupFormat !== 'raw') {
      return Query.prototype._convertGroupedData(result);
    }

    return result;
  }).catch(function(err) {
    return Promise.reject(Errors.create(err));
  })
};
...
```

#### <a name="apidoc.element.thinky.query.prototype._execute"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_execute (options, parse)](#apidoc.element.thinky.query.prototype._execute)
- description and source-code
```javascript
_execute = function (options, parse) {
  var self = this;
  options = options || {};
  var fullOptions = {groupFormat: 'raw'}
  util.loopKeys(options, function(options, key) {
    fullOptions[key] = options[key]
  });
  if (parse === true) {
    fullOptions.cursor = false;
  }

  if (self._model._error !== null) {
    return Promise.reject(self._model._error);
  }
  return self._model.ready().then(function() {
    return self._executeCallback(fullOptions, parse, options.groupFormat);
  });
}
```
- example usage
```shell
...
* asynchronous hooks).
*/
Query.prototype.run = function(options, callback) {
 if (typeof options === 'function') {
   callback = options;
   options = {};
 }
 return this._execute(options, true).nodeify(callback);
}


/**
* Execute a Query
* @param {Object=} options The options passed to the driver's method 'run'
* @param {Function=} callback
...
```

#### <a name="apidoc.element.thinky.query.prototype._executeCallback"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_executeCallback (fullOptions, parse, groupFormat)](#apidoc.element.thinky.query.prototype._executeCallback)
- description and source-code
```javascript
_executeCallback = function (fullOptions, parse, groupFormat) {
  var self = this;
  if (self._error !== undefined) {
    return Promise.reject(new Error("The partial value is not valid, so the write was not executed. The original error was:\n"+self
._error.message));
  }

  return self._query.run(fullOptions).then(function(result) {
    if (result === null && parse) {
      throw new Errors.DocumentNotFound();
    }

    // Expect a write result from RethinkDB
    if (self._postValidation === true) {
      return self._validateQueryResult(result);
    }

    if (result != null && typeof result.getType === 'function') {
      var resultType = result.getType();
      if (resultType === 'Feed' ||
        resultType === 'OrderByLimitFeed' ||
        resultType === 'UnionedFeed'
      ) {
        var feed = new Feed(result, self._model);
        return feed;
      }

      if (resultType === 'AtomFeed') {
        return result.next().then(function(initial) {
          var value = initial.new_val || {};
          return self._model._parse(value).then(function(doc) {
            doc._setFeed(result);
            return doc;
          });
        });
      }
    }

    if (parse === true) {
      return self._model._parse(result, self._ungroup);
    }

    if (groupFormat !== 'raw') {
      return Query.prototype._convertGroupedData(result);
    }

    return result;
  }).catch(function(err) {
    return Promise.reject(Errors.create(err));
  })
}
```
- example usage
```shell
...
  fullOptions.cursor = false;
}

if (self._model._error !== null) {
  return Promise.reject(self._model._error);
}
return self._model.ready().then(function() {
  return self._executeCallback(fullOptions, parse, options.groupFormat);
});
}

Query.prototype._executeCallback = function(fullOptions, parse, groupFormat) {
var self = this;
if (self._error !== undefined) {
  return Promise.reject(new Error("The partial value is not valid, so the write was not executed. The original error was:\n"+self
._error.message));
...
```

#### <a name="apidoc.element.thinky.query.prototype._get"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_get ()](#apidoc.element.thinky.query.prototype._get)
- description and source-code
```javascript
_get = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype._isPointWrite"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_isPointWrite ()](#apidoc.element.thinky.query.prototype._isPointWrite)
- description and source-code
```javascript
_isPointWrite = function () {
  return this._pointWrite || (Array.isArray(this._query._query) &&
      (this._query._query.length > 1) &&
      Array.isArray(this._query._query[1]) &&
      (this._query._query[1].length > 0) &&
      Array.isArray(this._query._query[1][0]) &&
      (this._query._query[1][0].length > 1) &&
      Array.isArray(this._query._query[1][0][1]) &&
      (this._query._query[1][0][1].length > 0) &&
      Array.isArray(this._query._query[1][0][1][0]) &&
      (this._query._query[1][0][1][0][0] === 16))
}
```
- example usage
```shell
...
Query.prototype._validateQueryResult = function(result) {
var self = this;
if (result.errors > 0) {
  console.log(result);
  return Promise.reject(new Errors.InvalidWrite("An error occured during the write", result));
}
if (!Array.isArray(result.changes)) {
  if (self._isPointWrite()) {
    return Promise.resolve();
  }
  return Promise.resolve([]);
}

var promises = [];
for(var i=0; i<result.changes.length; i++) {
...
```

#### <a name="apidoc.element.thinky.query.prototype._validateQueryResult"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_validateQueryResult (result)](#apidoc.element.thinky.query.prototype._validateQueryResult)
- description and source-code
```javascript
_validateQueryResult = function (result) {
  var self = this;
  if (result.errors > 0) {
    console.log(result);
    return Promise.reject(new Errors.InvalidWrite("An error occured during the write", result));
  }
  if (!Array.isArray(result.changes)) {
    if (self._isPointWrite()) {
      return Promise.resolve();
    }
    return Promise.resolve([]);
  }

  var promises = [];
  for(var i=0; i<result.changes.length; i++) {
    (function(i) {
      if (result.changes[i].new_val !== null) {
        promises.push(self._model._parse(result.changes[i].new_val));
      }
    })(i)
  }
  return Promise.all(promises).then(function(result) {
    if (self._isPointWrite()) {
      if (result.length > 1) {
        throw new Error('A point write returned multiple values')
      }
      return result[0];
    }
    return result;
  }).catch(function(error) {
    if (error instanceof Errors.DocumentNotFound) {
      // Should we send back null?
    }
    else {
      var revertPromises = [];
      var primaryKeys = [];
      var keysToValues = {};
      var r = self._model._thinky.r;
      for(var p=0; p<result.changes.length; p++) {
        // Extract the primary key of the document saved in the database
        var primaryKey = util.extractPrimaryKey(
            result.changes[p].old_val,
            result.changes[p].new_val,
            self._model._pk)
        if (primaryKey === undefined) {
          continue;
        }

        if (typeof primaryKey === "string") {
          keysToValues[primaryKey] = result.changes[p].old_val;
          primaryKeys.push(primaryKey);
        }
        else {
          // Replace documents with non-string type primary keys
          // one by one.
          revertPromises.push(r.table(self._model.getTableName())
            .get(primaryKey)
            .replace(result.changes[p].old_val)
            .run());
        }
      }

      // Replace all documents with string-type primary keys
      // in a single replace() operation.
      if (primaryKeys.length) {
        revertPromises.push(
          r.table(self._model.getTableName()).getAll(r.args(primaryKeys)).replace(function(doc) {
            return r.expr(keysToValues)(doc(self._model._pk));
          }).run()
        );
      }

      return Promise.all(revertPromises).then(function(result) {
        throw new Error("The write failed, and the changes were reverted.");
      }).error(function(error) {
        throw new Error("The write failed, and the attempt to revert the changes failed with the error:\n"+error.message);
      });
    }
  })
}
```
- example usage
```shell
...
  return self._query.run(fullOptions).then(function(result) {
if (result === null && parse) {
  throw new Errors.DocumentNotFound();
}

// Expect a write result from RethinkDB
if (self._postValidation === true) {
  return self._validateQueryResult(result);
}

if (result != null && typeof result.getType === 'function') {
  var resultType = result.getType();
  if (resultType === 'Feed' ||
    resultType === 'OrderByLimitFeed' ||
    resultType === 'UnionedFeed'
...
```

#### <a name="apidoc.element.thinky.query.prototype._validateUngroupResult"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>_validateUngroupResult (result)](#apidoc.element.thinky.query.prototype._validateUngroupResult)
- description and source-code
```javascript
_validateUngroupResult = function (result) {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.add"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>add ()](#apidoc.element.thinky.query.prototype.add)
- description and source-code
```javascript
add = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
      innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
      return r.branch(
        result.count().eq(1),
        r.object(key, innerQuery),
        r.branch(
          result.count().eq(0),
          {},
          r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
        )
      )
    }),
    {}
  )
});
break;
...
```

#### <a name="apidoc.element.thinky.query.prototype.addRelation"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>addRelation (field, joinedDocument)](#apidoc.element.thinky.query.prototype.addRelation)
- description and source-code
```javascript
addRelation = function (field, joinedDocument) {
  var self = this;
  var model = self._model;
  var joins = self._model._getModel()._joins;
  var joinedModel = joins[field].model;
  var r = self._model._thinky.r;

  switch (joins[field].type) {
    case 'hasOne':
    case 'hasMany':
      if (joinedDocument[joinedModel._pk] === undefined) {
        return new Query(model, self, {},
            new Error('Primary key for the joined document not found for a 'hasOne/hasMany' relation.')
        );
      }
      var updateValue = {};
      updateValue[joins[field].rightKey] = self._query(joins[field].leftKey);
      return joinedModel.get(joinedDocument[joinedModel._pk]).update(updateValue, {nonAtomic: true}).run()
    case 'belongsTo':
      var updateValue = {};
      if (joinedDocument[joins[field].rightKey] === undefined) {
        if (joinedDocument[joinedModel._pk] === undefined) {
          return new Query(model, self, {},
              new Error('The primary key or the joined key must be defined in the joined document for a 'belongsTo' relation.')
          );
        }
        updateValue[joins[field].leftKey] = joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey)._query
;
      }
      else {
        updateValue[joins[field].leftKey] = joinedDocument[joins[field].rightKey];
      }
      return self.update(updateValue, {nonAtomic: true}).run();
    case 'hasAndBelongsToMany':
      var linkModel = joins[field].linkModel;
      var linkValue;
      var link;
      if (joinedDocument[joins[field].rightKey] === undefined) {
        if (joinedDocument[joinedModel._pk] === undefined) {
          return new Query(model, self, {},
              new Error('The primary key or the joined key must be defined in the joined document for a 'hasAndBelongsToMany' relation
.')
          );
        }
        link = joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey)._query
      }
      else {
        link = r.expr(joinedDocument[joins[field].rightKey]);
      }

      if ((model.getTableName() === joinedModel.getTableName())
          && (joins[field].leftKey === joins[field].rightKey)) {
        linkValue = self._query(joins[field].leftKey).do(function(leftKey) {
          return link.do(function(rightKey) {
            return r.branch(
                rightKey.lt(leftKey),
                r.object(
                  'id', rightKey.add('_').add(leftKey),
                  joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
                ),
                r.object(
                  'id', leftKey.add('_').add(rightKey),
                  joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
                )
            )
          });
        });
      }
      else {
        linkValue = self._query(joins[field].leftKey).do(function(leftKey) {
          return link.do(function(rightKey) {
            if (model.getTableName() < joinedModel.getTableName()) {
              return r.object(
                'id', leftKey.add('_').add(rightKey),
                model.getTableName()+"_"+joins[field].leftKey, leftKey,
                joinedModel.getTableName()+"_"+joins[field].rightKey,rightKey
              )
            }
            else if (model.getTableName() > joinedModel.getTableName()) {
              return r.object(
                'id', rightKey.add('_').add(leftKey),
                model.getTableName()+"_"+joins[field].leftKey, leftKey,
                joinedModel.getTableName()+"_"+joins[field].rightKey,rightKey
              )
            }
            else {
              return r.branch(
                rightKey.lt(leftKey),
                r.object(
                  'id', leftKey.add('_').add(rightKey),
                  model.getTableName()+"_"+joins[field].leftKey, leftKey,
                  joinedModel.getTableName()+"_"+joins[field].rightKey,rightKey
                ),
                r.object(
                  'id', rightKey.add('_').add(leftKey),
                  model.getTableName()+"_"+joins[field].leftKey, leftKey, ...
```
- example usage
```shell
...
/**
* Add a relation
* @param {string} field The field of the joined document(s)
* @param {Object} joinedDocument An object with the primary key defined or the related key
* @return {Promise}
*
* hasOne, primary key required
* User.get(1).addRelation("account", {id: 2, sold: 2132})
* The promise resolved the document on which addRelation is called
*
* hasMany, primary key required
* User.get(1).addRelation("accounts", {id: 2, sold: 2132})
* The promise resolved the updated joined document
*
* belongsTo, right joined key OR primary key required
...
```

#### <a name="apidoc.element.thinky.query.prototype.and"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>and ()](#apidoc.element.thinky.query.prototype.and)
- description and source-code
```javascript
and = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.append"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>append ()](#apidoc.element.thinky.query.prototype.append)
- description and source-code
```javascript
append = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.april"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>april ()](#apidoc.element.thinky.query.prototype.april)
- description and source-code
```javascript
april = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.args"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>args ()](#apidoc.element.thinky.query.prototype.args)
- description and source-code
```javascript
args = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  }
}

// Replace all documents with string-type primary keys
// in a single replace() operation.
if (primaryKeys.length) {
  revertPromises.push(
    r.table(self._model.getTableName()).getAll(r.args(primaryKeys)).replace(function(doc) {
      return r.expr(keysToValues)(doc(self._model._pk));
    }).run()
  );
}

return Promise.all(revertPromises).then(function(result) {
  throw new Error("The write failed, and the changes were reverted.");
...
```

#### <a name="apidoc.element.thinky.query.prototype.asc"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>asc ()](#apidoc.element.thinky.query.prototype.asc)
- description and source-code
```javascript
asc = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.august"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>august ()](#apidoc.element.thinky.query.prototype.august)
- description and source-code
```javascript
august = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.avg"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>avg ()](#apidoc.element.thinky.query.prototype.avg)
- description and source-code
```javascript
avg = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.between"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>between ()](#apidoc.element.thinky.query.prototype.between)
- description and source-code
```javascript
between = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.binary"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>binary ()](#apidoc.element.thinky.query.prototype.binary)
- description and source-code
```javascript
binary = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.bindExecute"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bindExecute ()](#apidoc.element.thinky.query.prototype.bindExecute)
- description and source-code
```javascript
bindExecute = function () {
  var curriedArgs = Array.prototype.slice.call(arguments);
  return Function.prototype.bind.apply( Query.prototype.execute, [ this ].concat( curriedArgs ) );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.bindRun"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bindRun ()](#apidoc.element.thinky.query.prototype.bindRun)
- description and source-code
```javascript
bindRun = function () {
  var curriedArgs = Array.prototype.slice.call(arguments);
  return Function.prototype.bind.apply( Query.prototype.run, [ this ].concat( curriedArgs ) );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.bracket"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>bracket ()](#apidoc.element.thinky.query.prototype.bracket)
- description and source-code
```javascript
bracket = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  var updateValue = {};
  if (joinedDocument[joins[field].rightKey] === undefined) {
    if (joinedDocument[joinedModel._pk] === undefined) {
      return new Query(model, self, {},
          new Error('The primary key or the joined key must be defined in the joined document for a 'belongsTo' relation.')
      );
    }
    updateValue[joins[field].leftKey] = joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey)._query;
  }
  else {
    updateValue[joins[field].leftKey] = joinedDocument[joins[field].rightKey];
  }
  return self.update(updateValue, {nonAtomic: true}).run();
case 'hasAndBelongsToMany':
  var linkModel = joins[field].linkModel;
...
```

#### <a name="apidoc.element.thinky.query.prototype.branch"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>branch ()](#apidoc.element.thinky.query.prototype.branch)
- description and source-code
```javascript
branch = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
if (opts === undefined && util.isPlainObject(fn)) {
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
...
```

#### <a name="apidoc.element.thinky.query.prototype.catch"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>catch ()](#apidoc.element.thinky.query.prototype.catch)
- description and source-code
```javascript
catch = function () {
  var promise = this.run();
  return promise[key].apply(promise, arguments);
}
```
- example usage
```shell
...

if ((opts === undefined) && (util.isPlainObject(fn))) {
  opts = fn;
  fn = undefined;
}

return self._createIndex(name, fn, opts)
.catch(function(error) {
  self._getModel()._setError(error);
  throw error;
});
}

Model.prototype._createIndex = function(name, fn, opts) {
var model = this._getModel();
...
```

#### <a name="apidoc.element.thinky.query.prototype.ceil"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ceil ()](#apidoc.element.thinky.query.prototype.ceil)
- description and source-code
```javascript
ceil = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.changeAt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>changeAt ()](#apidoc.element.thinky.query.prototype.changeAt)
- description and source-code
```javascript
changeAt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.changes"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>changes ()](#apidoc.element.thinky.query.prototype.changes)
- description and source-code
```javascript
changes = function () {
  // In case of 'get().changes()' we want to remove the default(r.errror(...))
  // TODO: Do not hardcode this?
  if ((typeof this._query === 'function') && (this._query._query[0] === 92)) {
    this._query._query = this._query._query[1][0];
  }
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
    }
  })(key);
  break;

case 'changes':
  (function(key) {
    Query.prototype[key] = function() {
      // In case of 'get().changes()' we want to remove the default(r.errror(...))
      // TODO: Do not hardcode this?
      if ((typeof this._query === 'function') && (this._query._query[0] === 92)) {
        this._query._query = this._query._query[1][0];
      }
      return new Query(this._model, this._query[key].apply(this._query, arguments));
    }
  })(key);
...
```

#### <a name="apidoc.element.thinky.query.prototype.circle"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>circle ()](#apidoc.element.thinky.query.prototype.circle)
- description and source-code
```javascript
circle = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.coerceTo"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>coerceTo ()](#apidoc.element.thinky.query.prototype.coerceTo)
- description and source-code
```javascript
coerceTo = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
...
```

#### <a name="apidoc.element.thinky.query.prototype.concatMap"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>concatMap ()](#apidoc.element.thinky.query.prototype.concatMap)
- description and source-code
```javascript
concatMap = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
          break;

        case 'hasAndBelongsToMany':
          self._query = self._query.merge(function(doc) {
            if ((model.getTableName() === joins[key].model.getTableName()) && (joins[key].leftKey === joins[key].rightKey)) {
// In case the model is linked with itself on the same key

innerQuery = r.table(joins[key].link).getAll(doc(joins[key].leftKey), {index: joins[key].leftKey+"_"+joins[key].leftKey}).concatMap
(function(link) {
  return r.table(joins[key].model.getTableName()).getAll(
    r.branch(
      doc(joins[key].leftKey).eq(link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)),
      link(joins[key].leftKey+"_"+joins[key].leftKey).nth(1),
      link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)
    )
  , {index: joins[key].rightKey})
...
```

#### <a name="apidoc.element.thinky.query.prototype.config"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>config ()](#apidoc.element.thinky.query.prototype.config)
- description and source-code
```javascript
config = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.contains"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>contains ()](#apidoc.element.thinky.query.prototype.contains)
- description and source-code
```javascript
contains = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
...
```

#### <a name="apidoc.element.thinky.query.prototype.count"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>count ()](#apidoc.element.thinky.query.prototype.count)
- description and source-code
```javascript
count = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
  result.count().eq(1),
  r.object(key, innerQuery),
  r.branch(
    result.count().eq(0),
    {},
    r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
  )
)
...
```

#### <a name="apidoc.element.thinky.query.prototype.date"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>date ()](#apidoc.element.thinky.query.prototype.date)
- description and source-code
```javascript
date = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  if (schema.integer === true) { result.integer(); }
  return result;
case Boolean:
  result = type.boolean().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
  return result;
case Date:
  var result = type.date().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
  if (schema.min instanceof Date) { result.min(schema.min); }
  if (schema.max instanceof Date) { result.max(schema.max); }
  return result;
case Buffer:
  result = type.buffer().options(options).validator(schema.validator);
  if (schema.default !== undefined) { result.default(schema.default); }
...
```

#### <a name="apidoc.element.thinky.query.prototype.day"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>day ()](#apidoc.element.thinky.query.prototype.day)
- description and source-code
```javascript
day = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.dayOfWeek"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dayOfWeek ()](#apidoc.element.thinky.query.prototype.dayOfWeek)
- description and source-code
```javascript
dayOfWeek = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.dayOfYear"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dayOfYear ()](#apidoc.element.thinky.query.prototype.dayOfYear)
- description and source-code
```javascript
dayOfYear = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.db"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>db ()](#apidoc.element.thinky.query.prototype.db)
- description and source-code
```javascript
db = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.dbCreate"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbCreate ()](#apidoc.element.thinky.query.prototype.dbCreate)
- description and source-code
```javascript
dbCreate = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.dbDrop"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbDrop ()](#apidoc.element.thinky.query.prototype.dbDrop)
- description and source-code
```javascript
dbDrop = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.dbList"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>dbList ()](#apidoc.element.thinky.query.prototype.dbList)
- description and source-code
```javascript
dbList = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.december"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>december ()](#apidoc.element.thinky.query.prototype.december)
- description and source-code
```javascript
december = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.default"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>default ()](#apidoc.element.thinky.query.prototype.default)
- description and source-code
```javascript
default = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
// Note: We suppose that no method has an empty name
switch (key) {
  case 'get':
    // 'get' in thinky returns an error if the document is not found.
    // The driver currently just returns 'null'.
    (function(key) {
      Query.prototype[key] = function() {
        return new Query(this._model, this._query[key].apply(this._query, arguments)).default(this._r.error(new Errors.DocumentNotFound
().message));
      }
    })(key);
    // Copy it in '_get' without 'default'.
    (function(key) {
      Query.prototype['_get'] = function() {
        // Create a new query to let people fork it
        return new Query(this._model, this._query[key].apply(this._query, arguments));
...
```

#### <a name="apidoc.element.thinky.query.prototype.delay"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>delay ()](#apidoc.element.thinky.query.prototype.delay)
- description and source-code
```javascript
delay = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.delete"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>delete ()](#apidoc.element.thinky.query.prototype.delete)
- description and source-code
```javascript
delete = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
this._belongsTo = {};
this._hasOne = {};
this._hasMany = {};
// Example: { <linkTableName>: { <valueOfRightKey>: true, ... }, ... }
this._links = {}

// Keep reference of any doc having a link pointing to this
// So we can clean when users do doc.belongsToDoc.delete()
this._parents = {
  _hasOne: {},      // <tableName>: [{doc, key}]
  _hasMany: {},     // <tableName>: [{doc, key}]
  _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
  _belongsLinks: {} // <tableName>: [{doc, key}]
}
...
```

#### <a name="apidoc.element.thinky.query.prototype.deleteAt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>deleteAt ()](#apidoc.element.thinky.query.prototype.deleteAt)
- description and source-code
```javascript
deleteAt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.desc"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>desc ()](#apidoc.element.thinky.query.prototype.desc)
- description and source-code
```javascript
desc = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.difference"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>difference ()](#apidoc.element.thinky.query.prototype.difference)
- description and source-code
```javascript
difference = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.distance"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>distance ()](#apidoc.element.thinky.query.prototype.distance)
- description and source-code
```javascript
distance = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.distinct"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>distinct ()](#apidoc.element.thinky.query.prototype.distinct)
- description and source-code
```javascript
distinct = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.div"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>div ()](#apidoc.element.thinky.query.prototype.div)
- description and source-code
```javascript
div = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.do"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>do ()](#apidoc.element.thinky.query.prototype.do)
- description and source-code
```javascript
do = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
    return new Promise(function(resolve, reject) {
return r.branch(
  r.table(tableName).indexList().contains(name),
  r.table(tableName).indexWait(name),
  r.branch(
    r.table(tableName).info()('primary_key').eq(name),
    r.table(tableName).indexWait(name),
    r.table(tableName).indexCreate(name, fn, opts).do(function() {
      return r.table(tableName).indexWait(name);
    })
  )
)
.run()
.then(resolve)
.error(function(error) {
...
```

#### <a name="apidoc.element.thinky.query.prototype.downcase"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>downcase ()](#apidoc.element.thinky.query.prototype.downcase)
- description and source-code
```javascript
downcase = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.during"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>during ()](#apidoc.element.thinky.query.prototype.during)
- description and source-code
```javascript
during = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.epochTime"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>epochTime ()](#apidoc.element.thinky.query.prototype.epochTime)
- description and source-code
```javascript
epochTime = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.eq"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>eq ()](#apidoc.element.thinky.query.prototype.eq)
- description and source-code
```javascript
eq = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

  var promise = this.tableReady().then(function() {
return new Promise(function(resolve, reject) {
  return r.branch(
    r.table(tableName).indexList().contains(name),
    r.table(tableName).indexWait(name),
    r.branch(
      r.table(tableName).info()('primary_key').eq(name),
      r.table(tableName).indexWait(name),
      r.table(tableName).indexCreate(name, fn, opts).do(function() {
        return r.table(tableName).indexWait(name);
      })
    )
  )
  .run()
...
```

#### <a name="apidoc.element.thinky.query.prototype.eqJoin"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>eqJoin ()](#apidoc.element.thinky.query.prototype.eqJoin)
- description and source-code
```javascript
eqJoin = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.error"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>error ()](#apidoc.element.thinky.query.prototype.error)
- description and source-code
```javascript
error = function () {
  var promise = this.run();
  return promise[key].apply(promise, arguments);
}
```
- example usage
```shell
...
      }
    });

    //TODO Remove once
    self.getModel().ready().then(function() {
      Promise.all(promises).then(function() {
        self._onSavedBelongsTo(copy, docToSave, belongsToKeysSaved, saveAll, savedModel, resolve, reject);
      }).error(reject);
    });
  });
  return p;
}


/**
...
```

#### <a name="apidoc.element.thinky.query.prototype.execute"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>execute (options, callback)](#apidoc.element.thinky.query.prototype.execute)
- description and source-code
```javascript
execute = function (options, callback) {
  if (typeof options === 'function') {
    callback = options;
    options = {};
  }
  return this._execute(options, false).nodeify(callback);
}
```
- example usage
```shell
...

Model.prototype.run = function(options) {
var query = new Query(this);
return query.run(options);
}
Model.prototype.execute = function(options) {
var query = new Query(this);
return query.execute(options);
}

Model.prototype.save = function(docs, options) {
var self = this;
var r = self._getModel()._thinky.r;
var isArray = Array.isArray(docs);
...
```

#### <a name="apidoc.element.thinky.query.prototype.expr"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>expr ()](#apidoc.element.thinky.query.prototype.expr)
- description and source-code
```javascript
expr = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

return Promise.all([self.ready(), joinedModel.ready()]);
  }
};

(function() {
  // Import rethinkdbdash methods
  var Term = require('rethinkdbdash')({pool: false}).expr(1).__proto__;
  util.loopKeys(Term, function(Term, key) {
if (!Term.hasOwnProperty(key)) return;
if (key === 'run' || key[0] === '_') return;

(function(key) {
  switch (key) {
    case 'orderBy':
...
```

#### <a name="apidoc.element.thinky.query.prototype.february"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>february ()](#apidoc.element.thinky.query.prototype.february)
- description and source-code
```javascript
february = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.fill"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>fill ()](#apidoc.element.thinky.query.prototype.fill)
- description and source-code
```javascript
fill = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.filter"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>filter ()](#apidoc.element.thinky.query.prototype.filter)
- description and source-code
```javascript
filter = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.finally"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>finally ()](#apidoc.element.thinky.query.prototype.finally)
- description and source-code
```javascript
finally = function () {
  var promise = this.run();
  return promise[key].apply(promise, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.floor"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>floor ()](#apidoc.element.thinky.query.prototype.floor)
- description and source-code
```javascript
floor = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.fold"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>fold ()](#apidoc.element.thinky.query.prototype.fold)
- description and source-code
```javascript
fold = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.forEach"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>forEach ()](#apidoc.element.thinky.query.prototype.forEach)
- description and source-code
```javascript
forEach = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.friday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>friday ()](#apidoc.element.thinky.query.prototype.friday)
- description and source-code
```javascript
friday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.ge"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ge ()](#apidoc.element.thinky.query.prototype.ge)
- description and source-code
```javascript
ge = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.geojson"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>geojson ()](#apidoc.element.thinky.query.prototype.geojson)
- description and source-code
```javascript
geojson = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  else if (type.isPoint(schema)) {
if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
  var keys = Object.keys(doc).sort();
  if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
    return r.point(doc.longitude, doc.latitude)
  }
  else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
    return r.geojson(doc)
  }
}
else if (Array.isArray(doc)) {
  if ((doc.length === 2) && (typeof doc[0] === "number") && (typeof doc[1] === "number")) {
    return r.point(doc[0], doc[1])
  }
}
...
```

#### <a name="apidoc.element.thinky.query.prototype.get"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>get ()](#apidoc.element.thinky.query.prototype.get)
- description and source-code
```javascript
get = function () {
  return new Query(this._model, this._query[key].apply(this._query, arguments)).default(this._r.error(new Errors.DocumentNotFound
().message));
}
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.query.prototype.getAll"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getAll ()](#apidoc.element.thinky.query.prototype.getAll)
- description and source-code
```javascript
getAll = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  // Purge the database
  var promises = [];
  util.loopKeys(self._getModel()._joins, function(joins, field) {
var join = joins[field];
var joinedModel = join.model;

if ((join.type === 'hasOne') || (join.type === 'hasMany')) {
  promises.push(r.table(joinedModel.getTableName()).getAll(self[join.leftKey], {index: join.rightKey}).replace(function(doc) {
    return doc.without(join.rightKey)
  }).run())
}
// nothing to do for "belongsTo"
else if (join.type === 'hasAndBelongsToMany') {
  if (self.getModel()._getModel()._pk === join.leftKey) {
    // [1]
...
```

#### <a name="apidoc.element.thinky.query.prototype.getField"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getField ()](#apidoc.element.thinky.query.prototype.getField)
- description and source-code
```javascript
getField = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.getIntersecting"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getIntersecting ()](#apidoc.element.thinky.query.prototype.getIntersecting)
- description and source-code
```javascript
getIntersecting = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.getJoin"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getJoin (modelToGet, getAll, gotModel)](#apidoc.element.thinky.query.prototype.getJoin)
- description and source-code
```javascript
getJoin = function (modelToGet, getAll, gotModel) {
  var self = this;
  var r = self._model._getModel()._thinky.r;

  var model = this._model;
  var joins = this._model._getModel()._joins;

  var getAll = modelToGet === undefined;
  if (util.isPlainObject(modelToGet) === false) {
    modelToGet = {};
  }
  var innerQuery;

  gotModel = gotModel || {};
  gotModel[model.getTableName()] = true;

  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
                innerQuery = new Query(joins[key].model, result.nth(0));

                if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
                  innerQuery = modelToGet[key]._apply(innerQuery);
                }
                innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
                return r.branch(
                  result.count().eq(1),
                  r.object(key, innerQuery),
                  r.branch(
                    result.count().eq(0),
                    {},
                    r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").
add(key)))
                  )
                )
              }),
              {}
            )
          });
          break;

        case 'hasMany':
          self._query = self._query.merge(function(doc) {
            innerQuery = new Query(joins[key].model,
                       r.table(joins[key].model.getTableName())
                      .getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}))

            if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
              innerQuery = modelToGet[key]._apply(innerQuery);
            }
            innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel);
            if ((modelToGet[key] == null) || (modelToGet[key]._array !== false)) {
              innerQuery = innerQuery.coerceTo("ARRAY");
            }
            innerQuery = innerQuery._query;

            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.object(key, innerQuery),
              {}
            )
          });
          break;

        case 'hasAndBelongsToMany':
          self._query = self._query.merge(function(doc) {
            if ((model.getTableName() === joins[key].model.getTableName()) && (joins[key].leftKey === joins[key].rightKey)) {
              // In case the model is linked with itself on the same key

              innerQuery = r.table(joins[key].link).getAll(doc(joins[key].leftKey), {index: joins[key].leftKey+"_"+joins[key].leftKey
}).concatMap(function(link) {
                return r.table(joins[key].model.getTableName()).getAll(
                  r.branch(
                    doc(joins[key].leftKey).eq(link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)),
                    link(joins[key].leftKey+"_"+joins[key].leftKey).nth(1),
                    link(joins[key].leftKey+"_"+joins[key].leftKey).nth(0)
                  )
                , {index: joins[key].rightKey})
              });

              if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
                innerQuery = modelToGet[key]._apply(innerQuery);
              }

              if ((modelToGet[key] == null) || (modelToGet[key]._array !== false)) {
                innerQuery = innerQuery.coerceTo("ARRAY");
              }

              return r.branch(
                doc.hasFields(joins[key].leftKey),
                r.object(key, new Query(joins[key].model, innerQuery).getJoin(modelToGet[key], getAll, gotModel)._query),
                {}
              ) ...
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.query.prototype.getNearest"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>getNearest ()](#apidoc.element.thinky.query.prototype.getNearest)
- description and source-code
```javascript
getNearest = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.grant"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>grant ()](#apidoc.element.thinky.query.prototype.grant)
- description and source-code
```javascript
grant = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.group"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>group ()](#apidoc.element.thinky.query.prototype.group)
- description and source-code
```javascript
group = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.gt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>gt ()](#apidoc.element.thinky.query.prototype.gt)
- description and source-code
```javascript
gt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.hasFields"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>hasFields ()](#apidoc.element.thinky.query.prototype.hasFields)
- description and source-code
```javascript
hasFields = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
...
```

#### <a name="apidoc.element.thinky.query.prototype.hours"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>hours ()](#apidoc.element.thinky.query.prototype.hours)
- description and source-code
```javascript
hours = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.http"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>http ()](#apidoc.element.thinky.query.prototype.http)
- description and source-code
```javascript
http = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.inTimezone"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>inTimezone ()](#apidoc.element.thinky.query.prototype.inTimezone)
- description and source-code
```javascript
inTimezone = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.includes"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>includes ()](#apidoc.element.thinky.query.prototype.includes)
- description and source-code
```javascript
includes = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.indexCreate"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexCreate ()](#apidoc.element.thinky.query.prototype.indexCreate)
- description and source-code
```javascript
indexCreate = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
    return new Promise(function(resolve, reject) {
return r.branch(
  r.table(tableName).indexList().contains(name),
  r.table(tableName).indexWait(name),
  r.branch(
    r.table(tableName).info()('primary_key').eq(name),
    r.table(tableName).indexWait(name),
    r.table(tableName).indexCreate(name, fn, opts).do(function() {
      return r.table(tableName).indexWait(name);
    })
  )
)
.run()
.then(resolve)
.error(function(error) {
...
```

#### <a name="apidoc.element.thinky.query.prototype.indexDrop"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexDrop ()](#apidoc.element.thinky.query.prototype.indexDrop)
- description and source-code
```javascript
indexDrop = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.indexList"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexList ()](#apidoc.element.thinky.query.prototype.indexList)
- description and source-code
```javascript
indexList = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  opts = fn;
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
...
```

#### <a name="apidoc.element.thinky.query.prototype.indexRename"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexRename ()](#apidoc.element.thinky.query.prototype.indexRename)
- description and source-code
```javascript
indexRename = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.indexStatus"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexStatus ()](#apidoc.element.thinky.query.prototype.indexStatus)
- description and source-code
```javascript
indexStatus = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.indexWait"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexWait ()](#apidoc.element.thinky.query.prototype.indexWait)
- description and source-code
```javascript
indexWait = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  fn = undefined;
}

var promise = this.tableReady().then(function() {
  return new Promise(function(resolve, reject) {
    return r.branch(
      r.table(tableName).indexList().contains(name),
      r.table(tableName).indexWait(name),
      r.branch(
        r.table(tableName).info()('primary_key').eq(name),
        r.table(tableName).indexWait(name),
        r.table(tableName).indexCreate(name, fn, opts).do(function() {
          return r.table(tableName).indexWait(name);
        })
      )
...
```

#### <a name="apidoc.element.thinky.query.prototype.indexesOf"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>indexesOf ()](#apidoc.element.thinky.query.prototype.indexesOf)
- description and source-code
```javascript
indexesOf = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.info"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>info ()](#apidoc.element.thinky.query.prototype.info)
- description and source-code
```javascript
info = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

  var promise = this.tableReady().then(function() {
return new Promise(function(resolve, reject) {
  return r.branch(
    r.table(tableName).indexList().contains(name),
    r.table(tableName).indexWait(name),
    r.branch(
      r.table(tableName).info()('primary_key').eq(name),
      r.table(tableName).indexWait(name),
      r.table(tableName).indexCreate(name, fn, opts).do(function() {
        return r.table(tableName).indexWait(name);
      })
    )
  )
  .run()
...
```

#### <a name="apidoc.element.thinky.query.prototype.innerJoin"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>innerJoin ()](#apidoc.element.thinky.query.prototype.innerJoin)
- description and source-code
```javascript
innerJoin = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.insert"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>insert ()](#apidoc.element.thinky.query.prototype.insert)
- description and source-code
```javascript
insert = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

var querySaveSelf; // The query to save the document on which 'save'/'saveAll' was called.
// We haven't validated the document yet, so building the query with 'copy'
// may throw an error (for example if a Date has not a valid time).
var buildQuery = function () {
  if (self.__proto__._saved === false) {
    return querySaveSelf = r.table(constructor.getTableName())
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
      .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
...
```

#### <a name="apidoc.element.thinky.query.prototype.insertAt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>insertAt ()](#apidoc.element.thinky.query.prototype.insertAt)
- description and source-code
```javascript
insertAt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.intersects"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>intersects ()](#apidoc.element.thinky.query.prototype.intersects)
- description and source-code
```javascript
intersects = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>isEmpty ()](#apidoc.element.thinky.query.prototype.isEmpty)
- description and source-code
```javascript
isEmpty = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.january"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>january ()](#apidoc.element.thinky.query.prototype.january)
- description and source-code
```javascript
january = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.js"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>js ()](#apidoc.element.thinky.query.prototype.js)
- description and source-code
```javascript
js = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.json"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>json ()](#apidoc.element.thinky.query.prototype.json)
- description and source-code
```javascript
json = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.july"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>july ()](#apidoc.element.thinky.query.prototype.july)
- description and source-code
```javascript
july = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.june"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>june ()](#apidoc.element.thinky.query.prototype.june)
- description and source-code
```javascript
june = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.keys"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>keys ()](#apidoc.element.thinky.query.prototype.keys)
- description and source-code
```javascript
keys = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
      doc = numericDate;
    }
  }
  return new Date(doc); // Use r.ISO8601 and not 'new Date()' to keep timezone
}
else if (type.isPoint(schema)) {
  if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
    var keys = Object.keys(doc).sort();
    if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
      return r.point(doc.longitude, doc.latitude)
    }
    else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
      return r.geojson(doc)
    }
  }
...
```

#### <a name="apidoc.element.thinky.query.prototype.le"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>le ()](#apidoc.element.thinky.query.prototype.le)
- description and source-code
```javascript
le = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.limit"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>limit ()](#apidoc.element.thinky.query.prototype.limit)
- description and source-code
```javascript
limit = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.line"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>line ()](#apidoc.element.thinky.query.prototype.line)
- description and source-code
```javascript
line = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.literal"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>literal ()](#apidoc.element.thinky.query.prototype.literal)
- description and source-code
```javascript
literal = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.lt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>lt ()](#apidoc.element.thinky.query.prototype.lt)
- description and source-code
```javascript
lt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
}

if ((model.getTableName() === joinedModel.getTableName())
    && (joins[field].leftKey === joins[field].rightKey)) {
  linkValue = self._query(joins[field].leftKey).do(function(leftKey) {
    return link.do(function(rightKey) {
      return r.branch(
          rightKey.lt(leftKey),
          r.object(
            'id', rightKey.add('_').add(leftKey),
            joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
          ),
          r.object(
            'id', leftKey.add('_').add(rightKey),
            joins[field].leftKey+"_"+joins[field].leftKey, [leftKey, rightKey]
...
```

#### <a name="apidoc.element.thinky.query.prototype.map"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>map ()](#apidoc.element.thinky.query.prototype.map)
- description and source-code
```javascript
map = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
}

raw = raw || true;
if (raw === true) {
  return this._getModel()._listeners[eventKey];
}
else {
  return this._getModel()._listeners[eventKey].map(function(fn) {
    return fn.listener;
  });
}
}

Model.prototype.docSetMaxListeners = function(n) {
this._getModel()._maxListeners = n;
...
```

#### <a name="apidoc.element.thinky.query.prototype.march"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>march ()](#apidoc.element.thinky.query.prototype.march)
- description and source-code
```javascript
march = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.match"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>match ()](#apidoc.element.thinky.query.prototype.match)
- description and source-code
```javascript
match = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

/**
 * Creates an appropriate error given either an instance of Error or a message
 * from the RethinkDB driver
 */
errors.create = function(errorOrMessage) {
var message = (errorOrMessage instanceof Error) ? errorOrMessage.message : errorOrMessage;
if (message.match(errors.DOCUMENT_NOT_FOUND_REGEX)) {
  return new errors.DocumentNotFound(message);
} else if (message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)) {
  var primaryKey = message.match(errors.DUPLICATE_PRIMARY_KEY_REGEX)[1];
  return new errors.DuplicatePrimaryKey(message, primaryKey);
} else if (errorOrMessage instanceof Error) {
  return errorOrMessage;
}
...
```

#### <a name="apidoc.element.thinky.query.prototype.max"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>max ()](#apidoc.element.thinky.query.prototype.max)
- description and source-code
```javascript
max = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
options = util.mergeOptions(options, schema.options);
var result;
switch(schema._type) {
  case String:
    result = type.string().options(options).validator(schema.validator).enum(schema.enum);
    if (schema.default !== undefined) { result.default(schema.default); }
    if (typeof schema.min === "number") { result.min(schema.min); }
    if (typeof schema.max === "number") { result.max(schema.max); }
    if (typeof schema.length === "number") { result.length(schema.length); }
    if (schema.alphanum === true) { result.alphanum(); }
    if (schema.lowercase === true) { result.lowercase(); }
    if (schema.uppercase === true) { result.uppercase(); }
    if (typeof schema.regex === "string") { result.regex(regex, schema.flags); }
    return result;
  case Number:
...
```

#### <a name="apidoc.element.thinky.query.prototype.maxval"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>maxval ()](#apidoc.element.thinky.query.prototype.maxval)
- description and source-code
```javascript
maxval = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.may"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>may ()](#apidoc.element.thinky.query.prototype.may)
- description and source-code
```javascript
may = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.merge"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>merge ()](#apidoc.element.thinky.query.prototype.merge)
- description and source-code
```javascript
merge = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  gotModel[model.getTableName()] = true;

  util.loopKeys(joins, function(joins, key) {
    if (util.recurse(key, joins, modelToGet, getAll, gotModel)) {
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
...
```

#### <a name="apidoc.element.thinky.query.prototype.min"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>min ()](#apidoc.element.thinky.query.prototype.min)
- description and source-code
```javascript
min = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  content: String,
  idAuthor: String
});

// You can also add constraints on the schema
var Author = thinky.createModel("Author", {
  id: type.string(),      // a normal string
  name: type.string().min(2),  // a string of at least two characters
  email: type.string().email()  // a string that is a valid email
});

// Join the models
Post.belongsTo(Author, "author", "idAuthor", "id");
'''
...
```

#### <a name="apidoc.element.thinky.query.prototype.minutes"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>minutes ()](#apidoc.element.thinky.query.prototype.minutes)
- description and source-code
```javascript
minutes = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.minval"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>minval ()](#apidoc.element.thinky.query.prototype.minval)
- description and source-code
```javascript
minval = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.mod"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>mod ()](#apidoc.element.thinky.query.prototype.mod)
- description and source-code
```javascript
mod = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.monday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>monday ()](#apidoc.element.thinky.query.prototype.monday)
- description and source-code
```javascript
monday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.month"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>month ()](#apidoc.element.thinky.query.prototype.month)
- description and source-code
```javascript
month = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.mul"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>mul ()](#apidoc.element.thinky.query.prototype.mul)
- description and source-code
```javascript
mul = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.ne"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ne ()](#apidoc.element.thinky.query.prototype.ne)
- description and source-code
```javascript
ne = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.not"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>not ()](#apidoc.element.thinky.query.prototype.not)
- description and source-code
```javascript
not = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.november"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>november ()](#apidoc.element.thinky.query.prototype.november)
- description and source-code
```javascript
november = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.now"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>now ()](#apidoc.element.thinky.query.prototype.now)
- description and source-code
```javascript
now = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.nth"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>nth ()](#apidoc.element.thinky.query.prototype.nth)
- description and source-code
```javascript
nth = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
      switch (joins[key].type) {
        case 'hasOne':
        case 'belongsTo':
          self._query = self._query.merge(function(doc) {
            return r.branch(
              doc.hasFields(joins[key].leftKey),
              r.table(joins[key].model.getTableName()).getAll(doc(joins[key].leftKey), {index: joins[key].rightKey}).coerceTo("ARRAY
").do(function(result) {
innerQuery = new Query(joins[key].model, result.nth(0));

if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
  innerQuery = modelToGet[key]._apply(innerQuery);
}
innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
return r.branch(
  result.count().eq(1),
...
```

#### <a name="apidoc.element.thinky.query.prototype.object"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>object ()](#apidoc.element.thinky.query.prototype.object)
- description and source-code
```javascript
object = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...

  if ((modelToGet[key] != null) && (typeof modelToGet[key]._apply === 'function')) {
    innerQuery = modelToGet[key]._apply(innerQuery);
  }
  innerQuery = innerQuery.getJoin(modelToGet[key], getAll, gotModel)._query;
  return r.branch(
    result.count().eq(1),
    r.object(key, innerQuery),
    r.branch(
      result.count().eq(0),
      {},
      r.error(r.expr("More than one element found for ").add(doc.coerceTo("STRING")).add(r.expr("for the field ").add(key)))
    )
  )
}),
...
```

#### <a name="apidoc.element.thinky.query.prototype.october"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>october ()](#apidoc.element.thinky.query.prototype.october)
- description and source-code
```javascript
october = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.offsetsOf"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>offsetsOf ()](#apidoc.element.thinky.query.prototype.offsetsOf)
- description and source-code
```javascript
offsetsOf = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.or"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>or ()](#apidoc.element.thinky.query.prototype.or)
- description and source-code
```javascript
or = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.orderBy"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>orderBy ()](#apidoc.element.thinky.query.prototype.orderBy)
- description and source-code
```javascript
orderBy = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.outerJoin"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>outerJoin ()](#apidoc.element.thinky.query.prototype.outerJoin)
- description and source-code
```javascript
outerJoin = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.pluck"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>pluck ()](#apidoc.element.thinky.query.prototype.pluck)
- description and source-code
```javascript
pluck = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.point"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>point ()](#apidoc.element.thinky.query.prototype.point)
- description and source-code
```javascript
point = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  }
  return new Date(doc); // Use r.ISO8601 and not 'new Date()' to keep timezone
}
else if (type.isPoint(schema)) {
  if (util.isPlainObject(doc) && (doc['$reql_type$'] !== "GEOMETRY")) {
    var keys = Object.keys(doc).sort();
    if ((keys.length === 2) && (keys[0] === 'latitude') && (keys[1] === 'longitude') && (typeof doc.latitude === "number") && (typeof
 doc.longitude === "number")) {
      return r.point(doc.longitude, doc.latitude)
    }
    else if ((doc.type === "Point") && (Array.isArray(doc.coordinates)) && (doc.coordinates.length === 2)) { // Geojson
      return r.geojson(doc)
    }
  }
  else if (Array.isArray(doc)) {
    if ((doc.length === 2) && (typeof doc[0] === "number") && (typeof doc[1] === "number")) {
...
```

#### <a name="apidoc.element.thinky.query.prototype.polygon"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>polygon ()](#apidoc.element.thinky.query.prototype.polygon)
- description and source-code
```javascript
polygon = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.polygonSub"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>polygonSub ()](#apidoc.element.thinky.query.prototype.polygonSub)
- description and source-code
```javascript
polygonSub = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.prepend"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>prepend ()](#apidoc.element.thinky.query.prototype.prepend)
- description and source-code
```javascript
prepend = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.random"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>random ()](#apidoc.element.thinky.query.prototype.random)
- description and source-code
```javascript
random = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.range"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>range ()](#apidoc.element.thinky.query.prototype.range)
- description and source-code
```javascript
range = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.rebalance"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>rebalance ()](#apidoc.element.thinky.query.prototype.rebalance)
- description and source-code
```javascript
rebalance = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.reconfigure"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>reconfigure ()](#apidoc.element.thinky.query.prototype.reconfigure)
- description and source-code
```javascript
reconfigure = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.reduce"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>reduce ()](#apidoc.element.thinky.query.prototype.reduce)
- description and source-code
```javascript
reduce = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.removeRelation"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>removeRelation (field, joinedDocument)](#apidoc.element.thinky.query.prototype.removeRelation)
- description and source-code
```javascript
removeRelation = function (field, joinedDocument) {
  var self = this;
  var model = self._model;
  var joins = self._model._getModel()._joins;
  var joinedModel = joins[field].model;
  var r = self._model._thinky.r;

  var query;
  switch (joins[field].type) {
    case 'hasOne':
      query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
        return row.without(joins[field].rightKey)
      });
      query.setPostValidation();
      query.setPointWrite();
      return query;
    case 'hasMany':
      if (joinedDocument === undefined) {
        query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
          return row.without(joins[field].rightKey)
        })
      }
      else {
        query = joinedModel.getAll(r.expr(joinedDocument)(joinedModel._pk)).replace(function(row) {
          return row.without(joins[field].rightKey)
        })
      }
      query.setPostValidation();
      return query;
    case 'belongsTo':
      query = self.replace(function(row) {
        return row.without(joins[field].leftKey)
      })
      query.setPostValidation();
      return query;
    case 'hasAndBelongsToMany':
      var linkModel = joins[field].linkModel;
      if (joinedDocument === undefined) {
        query = self._query(joins[field].leftKey).do(function(leftKey) {
          // range are not supported at the moment, so keys is an object and we don't have to worry about empty sequences
          if ((model.getTableName() === joinedModel.getTableName())
              && (joins[field].leftKey === joins[field].rightKey)) {
            return linkModel.getAll(leftKey, {index: joins[field].leftKey+'_'+joins[field].leftKey}).delete()._query
          }
          else {
            return linkModel.getAll(leftKey, {index: model.getTableName()+'_'+joins[field].leftKey}).delete()._query
          }
        }).do(function(result) {
          return r.branch(
              result('errors').eq(0),
              true, // not relevant value
              r.error(result('errors'))
           )
        })
      }
      else {
        if (joinedDocument[joins[field].rightKey] === undefined) {
          if (joinedDocument[joinedModel._pk] === undefined) {
            return new Query(model, self, {},
                new Error('The primary key or the joined key must be defined in the joined document for a 'hasAndBelongsToMany'
relation.')
            );
          }

          if ((model.getTableName() === joinedModel.getTableName())
              && (joins[field].leftKey === joins[field].rightKey)) {
            query = self._query(joins[field].leftKey).do(function(leftKey) {
              return joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey).do(function(rightKey) {
                if (model.getTableName() < joinedModel.getTableName()) {
                  return linkModel.getAll(leftKey.add('_').add(rightKey)).delete()._query;
                }
                else if (model.getTableName() > joinedModel.getTableName()) {
                  return linkModel.getAll(rightKey.add('_').add(leftKey)).delete()._query;
                }
                else {
                  return r.branch(
                    leftKey.lt(rightKey),
                    linkModel.getAll(leftKey.add('_').add(rightKey)).delete()._query,
                    linkModel.getAll(rightKey.add('_').add(leftKey)).delete()._query
                  )
                }
              });
            })
          }
          else {
            query = self._query(joins[field].leftKey).do(function(leftKey) {
              return joinedModel.get(joinedDocument[joinedModel._pk]).bracket(joins[field].rightKey).do(function(rightKey) {
                if (model.getTableName() < joinedModel.getTableName()) {
                  return linkModel.getAll(leftKey.add('_').add(rightKey)).delete()._query
                }
                else if (model.getTableName() > joinedModel.getTableName()) {
                  return linkModel.getAll(rightKey.add('_ ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.replace"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>replace (value, options)](#apidoc.element.thinky.query.prototype.replace)
- description and source-code
```javascript
replace = function (value, options) {
  options = options || {};
  options.returnChanges = 'always';
  var error = null;
  var self = this;
  util.tryCatch(function() {
    if (util.isPlainObject(value)) {
      schemaUtil.validate(value, self._model._schema, '', {enforce_missing: false});
    }
  }, function(err) {
    error = err;
  });
  return new Query(this._model, this._query[key].call(this._query, value, options), {postValidation: true}, error);
}
```
- example usage
```shell
...
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
      .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
  }
}

self.getModel().ready().then(function() {
  util.tryCatch(function() {
    // Validate the document before saving it
    var promise = self.validate();
...
```

#### <a name="apidoc.element.thinky.query.prototype.round"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>round ()](#apidoc.element.thinky.query.prototype.round)
- description and source-code
```javascript
round = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.row"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>row ()](#apidoc.element.thinky.query.prototype.row)
- description and source-code
```javascript
row = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.run"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>run (options, callback)](#apidoc.element.thinky.query.prototype.run)
- description and source-code
```javascript
run = function (options, callback) {
  if (typeof options === 'function') {
    callback = options;
    options = {};
  }
  return this._execute(options, true).nodeify(callback);
}
```
- example usage
```shell
...
*/
});
'''

Retrieve the post with its author.

'''js
Post.get("0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a").getJoin().run().then(function(result) {
/*
result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.query.prototype.sample"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sample ()](#apidoc.element.thinky.query.prototype.sample)
- description and source-code
```javascript
sample = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.saturday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>saturday ()](#apidoc.element.thinky.query.prototype.saturday)
- description and source-code
```javascript
saturday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.seconds"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>seconds ()](#apidoc.element.thinky.query.prototype.seconds)
- description and source-code
```javascript
seconds = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.september"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>september ()](#apidoc.element.thinky.query.prototype.september)
- description and source-code
```javascript
september = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.setDifference"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setDifference ()](#apidoc.element.thinky.query.prototype.setDifference)
- description and source-code
```javascript
setDifference = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.setInsert"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setInsert ()](#apidoc.element.thinky.query.prototype.setInsert)
- description and source-code
```javascript
setInsert = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.setIntersection"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setIntersection ()](#apidoc.element.thinky.query.prototype.setIntersection)
- description and source-code
```javascript
setIntersection = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.setPointWrite"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setPointWrite ()](#apidoc.element.thinky.query.prototype.setPointWrite)
- description and source-code
```javascript
setPointWrite = function () {
  this._pointWrite = true;
}
```
- example usage
```shell
...
var query;
switch (joins[field].type) {
  case 'hasOne':
    query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
      return row.without(joins[field].rightKey)
    });
    query.setPostValidation();
    query.setPointWrite();
    return query;
  case 'hasMany':
    if (joinedDocument === undefined) {
      query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
        return row.without(joins[field].rightKey)
      })
    }
...
```

#### <a name="apidoc.element.thinky.query.prototype.setPostValidation"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setPostValidation ()](#apidoc.element.thinky.query.prototype.setPostValidation)
- description and source-code
```javascript
setPostValidation = function () {
  this._postValidation = true;
}
```
- example usage
```shell
...

var query;
switch (joins[field].type) {
  case 'hasOne':
    query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
      return row.without(joins[field].rightKey)
    });
    query.setPostValidation();
    query.setPointWrite();
    return query;
  case 'hasMany':
    if (joinedDocument === undefined) {
      query = joinedModel.getAll(self._query(joins[field].leftKey), {index: joins[field].rightKey}).replace(function(row) {
        return row.without(joins[field].rightKey)
      })
...
```

#### <a name="apidoc.element.thinky.query.prototype.setUnion"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>setUnion ()](#apidoc.element.thinky.query.prototype.setUnion)
- description and source-code
```javascript
setUnion = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.skip"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>skip ()](#apidoc.element.thinky.query.prototype.skip)
- description and source-code
```javascript
skip = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.slice"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>slice ()](#apidoc.element.thinky.query.prototype.slice)
- description and source-code
```javascript
slice = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
    return;
  }
  else {
    for(var k=0; k<field.length; k++) {
      if (virtual != null) {
        virtualValue = virtual[k];
      }
      generateVirtual(field[k], {path: defaultField.path.slice(j+1), value: defaultField.value}, this, virtualValue);
    }
  }
  keepGoing = false;
}
else {
  // field cannot be undefined (doc is not undefined on the first iteration, and we'll return if it becomes undefined
  field = field[path[j]];
...
```

#### <a name="apidoc.element.thinky.query.prototype.spliceAt"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>spliceAt ()](#apidoc.element.thinky.query.prototype.spliceAt)
- description and source-code
```javascript
spliceAt = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.split"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>split ()](#apidoc.element.thinky.query.prototype.split)
- description and source-code
```javascript
split = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.status"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>status ()](#apidoc.element.thinky.query.prototype.status)
- description and source-code
```javascript
status = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.sub"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sub ()](#apidoc.element.thinky.query.prototype.sub)
- description and source-code
```javascript
sub = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.sum"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sum ()](#apidoc.element.thinky.query.prototype.sum)
- description and source-code
```javascript
sum = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.sunday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sunday ()](#apidoc.element.thinky.query.prototype.sunday)
- description and source-code
```javascript
sunday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.sync"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>sync ()](#apidoc.element.thinky.query.prototype.sync)
- description and source-code
```javascript
sync = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.table"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>table ()](#apidoc.element.thinky.query.prototype.table)
- description and source-code
```javascript
table = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
});

var querySaveSelf; // The query to save the document on which 'save'/'saveAll' was called.
// We haven't validated the document yet, so building the query with 'copy'
// may throw an error (for example if a Date has not a valid time).
var buildQuery = function () {
  if (self.__proto__._saved === false) {
    return querySaveSelf = r.table(constructor.getTableName())
      .insert(copy, {returnChanges: 'always'})
  }
  else {
    if (copy[model._pk] === undefined) {
      throw new Error("The document was previously saved, but its primary key is undefined.");
    }
    return querySaveSelf = r.table(constructor.getTableName())
...
```

#### <a name="apidoc.element.thinky.query.prototype.tableCreate"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableCreate ()](#apidoc.element.thinky.query.prototype.tableCreate)
- description and source-code
```javascript
tableCreate = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
if (!this._initModel) return Promise.resolve();
if (this._tableReadyPromise) return this._tableReadyPromise;

// Create the table, or push the table name in the queue.
var r = model._thinky.r;
this._tableReadyPromise = model._thinky.dbReady()
.then(function() {
  return r.tableCreate(model._name, model._table).run();
})
.error(function(error) {
  if (error.message.match(/Table '.*' already exists/)) {
    return;
  }
  model._error = error;
  // Should we throw here?
...
```

#### <a name="apidoc.element.thinky.query.prototype.tableDrop"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableDrop ()](#apidoc.element.thinky.query.prototype.tableDrop)
- description and source-code
```javascript
tableDrop = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.tableList"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tableList ()](#apidoc.element.thinky.query.prototype.tableList)
- description and source-code
```javascript
tableList = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.then"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>then ()](#apidoc.element.thinky.query.prototype.then)
- description and source-code
```javascript
then = function () {
  var promise = this.run();
  return promise[key].apply(promise, arguments);
}
```
- example usage
```shell
...
email: "orphee@gmail.com"
});

// Join the documents
post.author = author;


post.saveAll().then(function(result) {
/*
post = result = {
  id: "0e4a6f6f-cc0c-4aa5-951a-fcfc480dd05a",
  title: "Hello World!",
  content: "This is an example.",
  idAuthor: "3851d8b4-5358-43f2-ba23-f4d481358901",
  author: {
...
```

#### <a name="apidoc.element.thinky.query.prototype.thursday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>thursday ()](#apidoc.element.thinky.query.prototype.thursday)
- description and source-code
```javascript
thursday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.time"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>time ()](#apidoc.element.thinky.query.prototype.time)
- description and source-code
```javascript
time = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.timeOfDay"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>timeOfDay ()](#apidoc.element.thinky.query.prototype.timeOfDay)
- description and source-code
```javascript
timeOfDay = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.timezone"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>timezone ()](#apidoc.element.thinky.query.prototype.timezone)
- description and source-code
```javascript
timezone = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toEpochTime"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toEpochTime ()](#apidoc.element.thinky.query.prototype.toEpochTime)
- description and source-code
```javascript
toEpochTime = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toGeojson"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toGeojson ()](#apidoc.element.thinky.query.prototype.toGeojson)
- description and source-code
```javascript
toGeojson = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toISO8601"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toISO8601 ()](#apidoc.element.thinky.query.prototype.toISO8601)
- description and source-code
```javascript
toISO8601 = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toJSON ()](#apidoc.element.thinky.query.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toJsonString"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toJsonString ()](#apidoc.element.thinky.query.prototype.toJsonString)
- description and source-code
```javascript
toJsonString = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toStream"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toStream ()](#apidoc.element.thinky.query.prototype.toStream)
- description and source-code
```javascript
toStream = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.toString"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>toString ()](#apidoc.element.thinky.query.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return this._query.toString();
}
```
- example usage
```shell
...
}

/**
 * Convert the query to its string representation.
 * @return {string}
 */
Query.prototype.toString = function() {
  return this._query.toString();
}

module.exports = Query;
...
```

#### <a name="apidoc.element.thinky.query.prototype.tuesday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>tuesday ()](#apidoc.element.thinky.query.prototype.tuesday)
- description and source-code
```javascript
tuesday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.typeOf"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>typeOf ()](#apidoc.element.thinky.query.prototype.typeOf)
- description and source-code
```javascript
typeOf = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.ungroup"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>ungroup ()](#apidoc.element.thinky.query.prototype.ungroup)
- description and source-code
```javascript
ungroup = function () {
  return new Query(this._model, this._query[key].apply(this._query, arguments), {ungroup: true});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.union"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>union ()](#apidoc.element.thinky.query.prototype.union)
- description and source-code
```javascript
union = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.upcase"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>upcase ()](#apidoc.element.thinky.query.prototype.upcase)
- description and source-code
```javascript
upcase = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.update"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>update (value, options)](#apidoc.element.thinky.query.prototype.update)
- description and source-code
```javascript
update = function (value, options) {
  options = options || {};
  options.returnChanges = 'always';
  var error = null;
  var self = this;
  util.tryCatch(function() {
    if (util.isPlainObject(value)) {
      schemaUtil.validate(value, self._model._schema, '', {enforce_missing: false});
    }
  }, function(err) {
    error = err;
  });
  return new Query(this._model, this._query[key].call(this._query, value, options), {postValidation: true}, error);
}
```
- example usage
```shell
...
  if (joinedDocument[joinedModel._pk] === undefined) {
    return new Query(model, self, {},
        new Error('Primary key for the joined document not found for a 'hasOne/hasMany' relation.')
    );
  }
  var updateValue = {};
  updateValue[joins[field].rightKey] = self._query(joins[field].leftKey);
  return joinedModel.get(joinedDocument[joinedModel._pk]).update(updateValue, {nonAtomic: true}).run()
case 'belongsTo':
  var updateValue = {};
  if (joinedDocument[joins[field].rightKey] === undefined) {
    if (joinedDocument[joinedModel._pk] === undefined) {
      return new Query(model, self, {},
          new Error('The primary key or the joined key must be defined in the joined document for a 'belongsTo' relation.')
      );
...
```

#### <a name="apidoc.element.thinky.query.prototype.uuid"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>uuid ()](#apidoc.element.thinky.query.prototype.uuid)
- description and source-code
```javascript
uuid = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.values"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>values ()](#apidoc.element.thinky.query.prototype.values)
- description and source-code
```javascript
values = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.wait"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>wait ()](#apidoc.element.thinky.query.prototype.wait)
- description and source-code
```javascript
wait = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.wednesday"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>wednesday ()](#apidoc.element.thinky.query.prototype.wednesday)
- description and source-code
```javascript
wednesday = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.withFields"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>withFields ()](#apidoc.element.thinky.query.prototype.withFields)
- description and source-code
```javascript
withFields = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.without"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>without ()](#apidoc.element.thinky.query.prototype.without)
- description and source-code
```javascript
without = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
...
  var promises = [];
  util.loopKeys(self._getModel()._joins, function(joins, field) {
var join = joins[field];
var joinedModel = join.model;

if ((join.type === 'hasOne') || (join.type === 'hasMany')) {
  promises.push(r.table(joinedModel.getTableName()).getAll(self[join.leftKey], {index: join.rightKey}).replace(function(doc) {
    return doc.without(join.rightKey)
  }).run())
}
// nothing to do for "belongsTo"
else if (join.type === 'hasAndBelongsToMany') {
  if (self.getModel()._getModel()._pk === join.leftKey) {
    // [1]
    promises.push(r.table(join.link).getAll(self[join.leftKey], {index: self.getModel().getTableName()+"_"+join.leftKey}).delete
().run())
...
```

#### <a name="apidoc.element.thinky.query.prototype.year"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>year ()](#apidoc.element.thinky.query.prototype.year)
- description and source-code
```javascript
year = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.query.prototype.zip"></a>[function <span class="apidocSignatureSpan">thinky.query.prototype.</span>zip ()](#apidoc.element.thinky.query.prototype.zip)
- description and source-code
```javascript
zip = function () {
  // Create a new query to let people fork it
  return new Query(this._model, this._query[key].apply(this._query, arguments));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.thinky.schema"></a>[module thinky.schema](#apidoc.module.thinky.schema)

#### <a name="apidoc.element.thinky.schema.generateDefault"></a>[function <span class="apidocSignatureSpan">thinky.schema.</span>generateDefault (doc, defaultField, originalDoc)](#apidoc.element.thinky.schema.generateDefault)
- description and source-code
```javascript
function generateDefault(doc, defaultField, originalDoc) {
  var path = defaultField.path;
  var value = defaultField.value;
  var field = doc;

  var keepGoing = true;
  for(var j=0; j<path.length-1; j++) {
    if (path[j] === arrayPrefix) {
      if (!Array.isArray(field)) {
        // This is caught by validate, except if there is an 'enforce_type: "none"'.
        return;
      }
      else {
        for(var k=0; k<field.length; k++) {
          generateDefault(field[k], {path: defaultField.path.slice(j+1), value: defaultField.value}, this);
        }
      }
      keepGoing = false;
    }
    else {
      field = field[path[j]];
      if (field === undefined) {
        // We do not populate parent of default fields by default
        return;
      }
    }
  }
  if (keepGoing && util.isPlainObject(field) && field[path[path.length-1]] === undefined) {
    if ((typeof value === "function") && !Array.isArray(value._query)) {
      field[path[path.length-1]] = value.call(doc);
    }
    else {
      if (util.isPlainObject(value) || Array.isArray(value)) {
        field[path[path.length-1]] = util.deepCopy(value);
      }
      else {
        field[path[path.length-1]] = value;
      }
    }
  }
  return doc;
}
```
- example usage
```shell
...

/**
 * Generate the default values for the document, first the non virtual fields, and then
 * the virtual fields.
 */
Document.prototype._generateDefault = function() {
  for(var i=0; i<this._getModel().defaultFields.length; i++) {
    schemaUtil.generateDefault(this, this._getModel().defaultFields[i], this);
  }
  if (this._getModel().virtualFields.length > 0) {
    this.generateVirtualValues();
  }
}
...
```

#### <a name="apidoc.element.thinky.schema.generateVirtual"></a>[function <span class="apidocSignatureSpan">thinky.schema.</span>generateVirtual (doc, defaultField, originalDoc, virtual)](#apidoc.element.thinky.schema.generateVirtual)
- description and source-code
```javascript
function generateVirtual(doc, defaultField, originalDoc, virtual) {
  var path = defaultField.path;
  var value = defaultField.value;
  var field = doc;

  var keepGoing = true;
  var virtualValue = virtual;

  for(var j=0; j<path.length-1; j++) {
    if (util.isPlainObject(virtualValue)) {
      virtualValue = virtualValue[path[j]];
    }
    else {
      virtualValue = undefined;
    }

    if (path[j] === arrayPrefix) {
      if (!Array.isArray(field)) {
        // This is caught by validate, except if there is an 'enforce_type: "none"'.
        return;
      }
      else {
        for(var k=0; k<field.length; k++) {
          if (virtual != null) {
            virtualValue = virtual[k];
          }
          generateVirtual(field[k], {path: defaultField.path.slice(j+1), value: defaultField.value}, this, virtualValue);
        }
      }
      keepGoing = false;
    }
    else {
      // field cannot be undefined (doc is not undefined on the first iteration, and we'll return if it becomes undefined
      field = field[path[j]];
      if (field === undefined) {
        // We do not populate parent of default fields by default
        return;
      }
    }
  }
  if (keepGoing) {
    if (value === undefined) {
      if (util.isPlainObject(virtualValue) && (virtualValue[[path[path.length-1]]] !== undefined)) {
        field[path[path.length-1]] = virtualValue[[path[path.length-1]]];
      }
    }
    else if ((typeof value === "function") && !Array.isArray(value._query)) {
      field[path[path.length-1]] = value.call(doc);
    }
    else {
      if (util.isPlainObject(value)) {
        field[path[path.length-1]] = util.deepCopy(value);
      }
      else if (value !== undefined) {
        field[path[path.length-1]] = value;
      }
    }
  }
  return doc;
}
```
- example usage
```shell
...
/**
* Generate the virtual values for the document, or re-inject the ones
* previously saved.
* This should be called **after** '_generateDefault'.
*/
Document.prototype.generateVirtualValues = function() {
 for(var i=0; i<this._getModel().virtualFields.length; i++) {
   schemaUtil.generateVirtual(this, this._getModel().virtualFields[i], this, this._getVirtual());
 }
}


/**
* Generate the default values for the document, first the non virtual fields, and then
* the virtual fields.
...
```

#### <a name="apidoc.element.thinky.schema.parse"></a>[function <span class="apidocSignatureSpan">thinky.schema.</span>parse (schema, prefix, options, model)](#apidoc.element.thinky.schema.parse)
- description and source-code
```javascript
function parse(schema, prefix, options, model) {
  var result;

  if ((prefix === '') && (type.isObject(schema) === false) && (util.isPlainObject(schema) === false)) {
    throw new Errors.ValidationError("The schema must be a plain object.")
  }

  // Validate a schema and add the field _enum if needed
  if (util.isPlainObject(schema)) {
    if (schema._type !== undefined) {
      options = util.mergeOptions(options, schema.options);
      var result;
      switch(schema._type) {
        case String:
          result = type.string().options(options).validator(schema.validator).enum(schema.enum);
          if (schema.default !== undefined) { result.default(schema.default); }
          if (typeof schema.min === "number") { result.min(schema.min); }
          if (typeof schema.max === "number") { result.max(schema.max); }
          if (typeof schema.length === "number") { result.length(schema.length); }
          if (schema.alphanum === true) { result.alphanum(); }
          if (schema.lowercase === true) { result.lowercase(); }
          if (schema.uppercase === true) { result.uppercase(); }
          if (typeof schema.regex === "string") { result.regex(regex, schema.flags); }
          return result;
        case Number:
          result = type.number().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          if (typeof schema.min === "number") { result.min(schema.min); }
          if (typeof schema.max === "number") { result.max(schema.max); }
          if (typeof schema.length === "number") { result.length(schema.length); }
          if (schema.integer === true) { result.integer(); }
          return result;
        case Boolean:
          result = type.boolean().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          return result;
        case Date:
          var result = type.date().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          if (schema.min instanceof Date) { result.min(schema.min); }
          if (schema.max instanceof Date) { result.max(schema.max); }
          return result;
        case Buffer:
          result = type.buffer().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          return result
        case Object:
          result = type.object().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          util.loopKeys(schema.schema, function(_schema, key) {
            result.setKey(key, parse(_schema[key], prefix+"["+key+"]", options));
          })
          if (prefix === '') {
            result._setModel(model)
          }
          return result;
        case Array:
          var result = type.array().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          if (schema.schema !== undefined) {
            result.schema(parse(schema.schema, prefix+"[0]", options));
          }
          if (typeof schema.min === "number") { result.min(schema.min); }
          if (typeof schema.max === "number") { result.max(schema.max); }
          if (typeof schema.length === "number") { result.length(schema.length); }
          return result;
        case 'Point':
          result = type.point().options(options).validator(schema.validator);
          if (schema.default !== undefined) { result.default(schema.default); }
          return result;
        case 'virtual':
          result = type.virtual();
          if (schema.default !== undefined) { result.default(schema.default); }
          return result
        default: // Unknown type
          throw new Errors.ValidationError("The field '_type' must be 'String'/'Number'/'Boolean'/'Date'/'Buffer'/'Object'/'Array
'/''virtual''/''Point'' for "+prefix);
      }
    }
    else if (type.isString(sc ...
```
- example usage
```shell
...
this._options = {};
this._options.enforce_missing = (options.enforce_missing != null) ? options.enforce_missing : thinky._options.enforce_missing;
this._options.enforce_extra = (options.enforce_extra != null) ? options.enforce_extra : thinky._options.enforce_extra;
this._options.enforce_type = (options.enforce_type != null) ? options.enforce_type : thinky._options.enforce_type;
this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : thinky._options.timeFormat;
this._options.validate = (options.validate != null) ? options.validate : thinky._options.validate;

this._schema = schemaUtil.parse(schema, '', this._options, this);
//console.log(JSON.stringify(this._schema, null, 2));

this.virtualFields = [];
this.defaultFields = [];
this._schema._getDefaultFields([], this.defaultFields, this.virtualFields)

this.needToGenerateFields = (this.defaultFields.length+this.virtualFields.length) !== 0;
...
```

#### <a name="apidoc.element.thinky.schema.validate"></a>[function <span class="apidocSignatureSpan">thinky.schema.</span>validate (doc, schema, prefix, options)](#apidoc.element.thinky.schema.validate)
- description and source-code
```javascript
function validate(doc, schema, prefix, options) {
  schema.validate(doc, prefix, options);
}
```
- example usage
```shell
...
* @param {Object=} modelToValidate Internal parameter, model to validate
* @return {Promise=} return a promise if the validation is asynchrone, else undefined.
*/
Document.prototype.validateAll = function(options, modelToValidate) {
 var validateAll = modelToValidate === undefined;
 modelToValidate = modelToValidate || {};

 return this.validate(options, modelToValidate, validateAll, {}, '', true);
}


/*
* Internal methods that will validate the document (but that will not execute the hooks).
* @param {Object=} options Options to overwrite the ones of the document.
* @param {Object=} modelToValidate Internal parameter, model to validate
...
```



# <a name="apidoc.module.thinky.util"></a>[module thinky.util](#apidoc.module.thinky.util)

#### <a name="apidoc.element.thinky.util.bindEmitter"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>bindEmitter (self)](#apidoc.element.thinky.util.bindEmitter)
- description and source-code
```javascript
function bindEmitter(self) {
  util.loopKeys(EventEmitter.prototype, function(emitter, key) {
    var fn = emitter[key];
    if (typeof fn === 'function') {
      self[key] = function() {
        var args = new Array(arguments.length);
        for(var i = 0; i < arguments.length; i++) {
          args[i] = arguments[i];
        }
        fn.apply(self, args);
      }
    }
  });
}
```
- example usage
```shell
...
options = options || {};
this._options = {};
this._options.timeFormat = (options.timeFormat != null) ? options.timeFormat : model.getOptions().timeFormat;
this._options.validate = (options.validate != null) ? options.validate : model.getOptions().validate;

this._saved = options.saved || false;  // Whether the document is saved or not

util.bindEmitter(self);  // Copy methods from eventEmitter

// links to hasOne/hasMany documents
// We use it to know if some links have been removed/added before saving.
// Example: { key: doc } or { key: [docs] }
this._belongsTo = {};
this._hasOne = {};
this._hasMany = {};
...
```

#### <a name="apidoc.element.thinky.util.changeProto"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>changeProto (object, newProto)](#apidoc.element.thinky.util.changeProto)
- description and source-code
```javascript
function changeProto(object, newProto) {
  object.__proto__ = newProto;
}
```
- example usage
```shell
...
  throw new Error("Cannot build a new instance of '"+proto._name+"' without an object")
}
// We create a deepcopy only if doc was already used to create a document
if (doc instanceof Document) {
  doc = util.deepCopy(doc);
}

util.changeProto(doc, new Document(model, options));

// Create joins document. We do it here because 'options' are easily available
util.loopKeys(proto._joins, function(joins, key) {
  if (doc[key] != null) {
    if ((joins[key].type === 'hasOne') && (doc[key] instanceof Document === false)) {
      doc[key] = new joins[key].model(doc[key], options);
    }
...
```

#### <a name="apidoc.element.thinky.util.deepCopy"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>deepCopy (value)](#apidoc.element.thinky.util.deepCopy)
- description and source-code
```javascript
function deepCopy(value) {
  var result;
  if (value instanceof Buffer) {
    // isPlainObject(buffer) returns true.
    return new Buffer(value);
  }

  if (isPlainObject(value) === true) {
    result = {};
    loopKeys(value, function(_value, key) {
      if (_value.hasOwnProperty(key)) {
        result[key] = deepCopy(_value[key]);
      }
    });
    return result;
  }

  if (Array.isArray(value)) {
    result = []
    for(var i=0; i<value.length; i++) {
      result.push(deepCopy(value[i]));
    }
    return result;
  }

  return value;
}
```
- example usage
```shell
...
 // when virtual fields are nested in arrays.
 // This implementation still allows no overhead if no virtual fields exist,
 // which should be the most common case
 for(var i=0; i<this._getModel().virtualFields.length; i++) {
   var key = this._getModel().virtualFields[i].path[0];
   copy[key] = this[key];
 }
 this.__proto__.virtualValue = util.deepCopy(copy);
}


/**
* Get the virtual fields saved by '_saveVirtual'.
* @return {Object=}
*/
...
```

#### <a name="apidoc.element.thinky.util.extraField"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>extraField (prefix, key)](#apidoc.element.thinky.util.extraField)
- description and source-code
```javascript
function extraField(prefix, key) {
  if (prefix === '') {
    throw new Errors.ValidationError("Extra field '"+key+"' not allowed.")
  }
  throw new Errors.ValidationError("Extra field '"+key+"' in "+prefix+" not allowed.")
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.util.extractPrimaryKey"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>extractPrimaryKey (oldValue, newValue, primaryKey)](#apidoc.element.thinky.util.extractPrimaryKey)
- description and source-code
```javascript
function extractPrimaryKey(oldValue, newValue, primaryKey) {
  var primaryKey;
  if (oldValue !== null) {
    return oldValue[primaryKey];
  }
  if (newValue !== null) {
    return newValue[primaryKey];
  }
  return undefined;
}
```
- example usage
```shell
...
    else {
var revertPromises = [];
var primaryKeys = [];
var keysToValues = {};
var r = self._model._thinky.r;
for(var p=0; p<result.changes.length; p++) {
  // Extract the primary key of the document saved in the database
  var primaryKey = util.extractPrimaryKey(
      result.changes[p].old_val,
      result.changes[p].new_val,
      self._model._pk)
  if (primaryKey === undefined) {
    continue;
  }
...
```

#### <a name="apidoc.element.thinky.util.hook"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>hook (options)](#apidoc.element.thinky.util.hook)
- description and source-code
```javascript
function hook(options) {
  var preHooks = options.preHooks;
  if (Array.isArray(preHooks) === false) {
    preHooks = [];
  }
  var postHooks = options.postHooks;
  if (Array.isArray(postHooks) === false) {
    postHooks = [];
  }
  var doc = options.doc; // We need the doc to set the context of the hooks
  var async = options.async || false;
  var fn = options.fn; // The function that we are hook
  var fnArgs = options.fnArgs;

  if (async === true) {
    return new Promise(function(resolve, reject) {
      _asyncHook({
        resolve: resolve,
        reject: reject,
        preHooks: preHooks,
        postHooks: postHooks,
        doc: doc,
        fn: fn,
        fnArgs: fnArgs
      });
    });
  }

  return _syncHook({
    preHooks: preHooks,
    postHooks: postHooks,
    doc: doc,
    fn: fn,
    fnArgs: fnArgs
  });
}
```
- example usage
```shell
...

var self = this;
var validatedModelCopy = util.deepCopy(validatedModel);

//TODO: Can we not always call this?
var async = self._validateIsAsync(modelToValidate, validateAll, validatedModelCopy);

return util.hook({
  preHooks: self._getModel()._pre.validate,
  postHooks: self._getModel()._post.validate,
  doc: self,
  async: async,
  fn: self._validateHook,
  fnArgs: [options, modelToValidate, validateAll, validatedModel, prefix]
})
...
```

#### <a name="apidoc.element.thinky.util.isPlainObject"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>isPlainObject (obj)](#apidoc.element.thinky.util.isPlainObject)
- description and source-code
```javascript
function isPlainObject(obj) {
  return Object.prototype.toString.call(obj) === '[object Object]';
}
```
- example usage
```shell
...
var self = this;  // Keep a reference to itself.

this.constructor = model;  // The constructor for this model
this._model = model._getModel(); // The instance of Model

// We don't want to store options if they are different
// than the one provided by the model
if (util.isPlainObject(options)) {
  this._schemaOptions = {};
  this._schemaOptions.enforce_missing =
      (options.enforce_missing != null) ? options.enforce_missing : model.getOptions().enforce_missing;
  this._schemaOptions.enforce_extra =
      (options.enforce_extra != null) ? options.enforce_extra : model.getOptions().enforce_extra;
  this._schemaOptions.enforce_type =
      (options.enforce_type != null) ? options.enforce_type : model.getOptions().enforce_type;
...
```

#### <a name="apidoc.element.thinky.util.loopKeys"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>loopKeys (obj, fn)](#apidoc.element.thinky.util.loopKeys)
- description and source-code
```javascript
function loopKeys(obj, fn) {
  if (isPlainObject(obj)) {
    var keys = Object.keys(obj);
    var result;
    for(var i=0; i<keys.length; i++) {
      result = fn(obj, keys[i]);
      if (result === false) return;
    }
  }
}
```
- example usage
```shell
...
  _hasOne: {},      // <tableName>: [{doc, key}]
  _hasMany: {},     // <tableName>: [{doc, key}]
  _belongsTo: {},   // <tableName>: [{doc, key, foreignKey}]
  _belongsLinks: {} // <tableName>: [{doc, key}]
}

// Bind listeners of the model to this documents.
util.loopKeys(model._listeners, function(listeners, eventKey) {
  for(var j=0; j<listeners[eventKey].length; j++) {
    if (listeners[eventKey][j].once === false) {
      self.addListener(eventKey, listeners[eventKey][j].listener);
    }
    else if (listeners[eventKey][j].once === true) {
      self.once(eventKey, listeners[eventKey][j].listener);
    }
...
```

#### <a name="apidoc.element.thinky.util.looseType"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>looseType (prefix, expected)](#apidoc.element.thinky.util.looseType)
- description and source-code
```javascript
function looseType(prefix, expected) {
  if ((expected.length > 0) && (vowels[expected[0]])) {
    throw new Errors.ValidationError("Value for "+prefix+" must be an "+expected+" or null.")
  }
  throw new Errors.ValidationError("Value for "+prefix+" must be a "+expected+" or null.")
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.util.mergeOptions"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>mergeOptions (options, newOptions)](#apidoc.element.thinky.util.mergeOptions)
- description and source-code
```javascript
function mergeOptions(options, newOptions) {
  if (util.isPlainObject(newOptions)) {
    if (!options) {
      options = {};
    }
    var localOptions = {};
    localOptions.enforce_missing = (newOptions.enforce_missing != null) ? newOptions.enforce_missing : options.enforce_missing;
    localOptions.enforce_type = (newOptions.enforce_type != null) ? newOptions.enforce_type : options.enforce_type;
    localOptions.enforce_extra = (newOptions.enforce_extra != null) ? newOptions.enforce_extra : options.enforce_extra;
    return localOptions;
  }
  return options;
}
```
- example usage
```shell
...
Document.prototype._validateHook = function(options, modelToValidate, validateAll, validatedModel, prefix) {
var self = this;
var promises = [];
var error;

var schemaOptions = self._getSchemaOptions();
if (util.isPlainObject(schemaOptions)) {
  schemaOptions = util.mergeOptions(schemaOptions, options);
}
else {
  schemaOptions = options;
}


if (typeof self._getModel()._validator === 'function') {
...
```

#### <a name="apidoc.element.thinky.util.pseudoTypeError"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>pseudoTypeError (type, missingField, prefix)](#apidoc.element.thinky.util.pseudoTypeError)
- description and source-code
```javascript
function pseudoTypeError(type, missingField, prefix) {
  throw new Errors.ValidationError("The raw "+type+" object for "+prefix+" is missing the required field "+missingField+".")
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.util.recurse"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>recurse (key, joins, modelTo, all, done)](#apidoc.element.thinky.util.recurse)
- description and source-code
```javascript
function recurse(key, joins, modelTo, all, done) {
  return (util.isPlainObject(modelTo) && modelTo.hasOwnProperty(key))
    || ((all === true) && (done[joins[key].model.getTableName()] !== true))
}
```
- example usage
```shell
...
}

var constructor = self.__proto__.constructor;
validatedModel[constructor.getTableName()] = true;

// Validate joined documents
util.loopKeys(self._getModel()._joins, function(joins, key) {
  if (util.recurse(key, joins, modelToValidate, validateAll, validatedModel)) {
    switch (joins[key].type) {
      case 'hasOne':
      case 'belongsTo':
        if (util.isPlainObject(self[key])) {
          if (self[key] instanceof Document === false) {
            self[key] = new self._getModel()._joins[key].model(self[key]);
          }
...
```

#### <a name="apidoc.element.thinky.util.strictType"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>strictType (prefix, expected)](#apidoc.element.thinky.util.strictType)
- description and source-code
```javascript
function strictType(prefix, expected) {
  if ((expected.length > 0) && (vowels[expected[0]])) {
    throw new Errors.ValidationError("Value for "+prefix+" must be an "+expected+".")
  }
  throw new Errors.ValidationError("Value for "+prefix+" must be a "+expected+".")
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.util.toArray"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>toArray (args)](#apidoc.element.thinky.util.toArray)
- description and source-code
```javascript
function toArray(args) {
    return Array.prototype.slice.call(args);
}
```
- example usage
```shell
...
        self._makeEmitter();
        setImmediate(function() {
          self.feed._each(self._eachCb.bind(self), function() {
            self._eventEmitter.emit('end');
          });
        });
      }
      self._eventEmitter[method].apply(self._eventEmitter, util.toArray(arguments));
    };
  })(i);
}

module.exports = Feed;
...
```

#### <a name="apidoc.element.thinky.util.tryCatch"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>tryCatch (toTry, handleError)](#apidoc.element.thinky.util.tryCatch)
- description and source-code
```javascript
function tryCatch(toTry, handleError) {
  try{
    toTry()
  }
  catch(err) {
    handleError(err)
  }
}
```
- example usage
```shell
...
    }
    return querySaveSelf = r.table(constructor.getTableName())
      .get(copy[model._pk]).replace(copy, {returnChanges: 'always'})
  }
}

self.getModel().ready().then(function() {
  util.tryCatch(function() {
    // Validate the document before saving it
    var promise = self.validate();
    if (promise instanceof Promise) {
      promise.then(function() {
        querySaveSelf = buildQuery();
        querySaveSelf.run().then(function(result) {
          self._onSaved(result, docToSave, saveAll, savedModel, resolve, reject)
...
```

#### <a name="apidoc.element.thinky.util.undefinedField"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>undefinedField (prefix)](#apidoc.element.thinky.util.undefinedField)
- description and source-code
```javascript
function undefinedField(prefix) {
  throw new Errors.ValidationError("Value for "+prefix+" must be defined.")
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.thinky.util.validateIfUndefined"></a>[function <span class="apidocSignatureSpan">thinky.util.</span>validateIfUndefined (value, prefix, type, options)](#apidoc.element.thinky.util.validateIfUndefined)
- description and source-code
```javascript
function validateIfUndefined(value, prefix, type, options) {
  if (value === undefined) {
    if (options.enforce_missing === true) {
      undefinedField(prefix);
    }
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
