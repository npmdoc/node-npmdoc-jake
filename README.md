# api documentation for  [jake (v8.0.15)](https://github.com/jakejs/jake#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-jake.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jake) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jake.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jake)
#### JavaScript build tool, similar to Make or Rake

[![NPM](https://nodei.co/npm/jake.png?downloads=true)](https://www.npmjs.com/package/jake)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jake/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jake_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jake/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jake/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jake/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matthew Eernisse",
        "email": "mde@fleegix.org",
        "url": "http://fleegix.org"
    },
    "bin": {
        "jake": "./bin/cli.js"
    },
    "bugs": {
        "url": "https://github.com/jakejs/jake/issues"
    },
    "dependencies": {
        "async": "0.9.x",
        "chalk": "0.4.x",
        "filelist": "0.0.x",
        "minimatch": "3.x",
        "utilities": "1.0.x"
    },
    "description": "JavaScript build tool, similar to Make or Rake",
    "devDependencies": {
        "q": "0.9.x"
    },
    "directories": {},
    "dist": {
        "shasum": "f0da7d58e790ac1a8f86e6ee0f193e5d9230eabb",
        "tarball": "https://registry.npmjs.org/jake/-/jake-8.0.15.tgz"
    },
    "engines": {
        "node": "*"
    },
    "homepage": "https://github.com/jakejs/jake#readme",
    "keywords": [
        "build",
        "cli",
        "make",
        "rake"
    ],
    "license": "Apache-2.0",
    "main": "./lib/jake.js",
    "maintainers": [
        {
            "name": "benng",
            "email": "me@benng.me"
        },
        {
            "name": "danfinlay",
            "email": "dan@danfinlay.com"
        },
        {
            "name": "mde",
            "email": "mde@fleegix.org"
        },
        {
            "name": "ondrej",
            "email": "info@anzui.de"
        }
    ],
    "name": "jake",
    "optionalDependencies": {},
    "preferGlobal": true,
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jakejs/jake.git"
    },
    "scripts": {
        "test": "./bin/cli.js test"
    },
    "version": "8.0.15"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jake](#apidoc.module.jake)
1.  [function <span class="apidocSignatureSpan">jake.</span>DirectoryTask (name)](#apidoc.element.jake.DirectoryTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>EventBuffer (src, events)](#apidoc.element.jake.EventBuffer)
1.  [function <span class="apidocSignatureSpan">jake.</span>Exec ()](#apidoc.element.jake.Exec)
1.  [function <span class="apidocSignatureSpan">jake.</span>FileList ()](#apidoc.element.jake.FileList)
1.  [function <span class="apidocSignatureSpan">jake.</span>FileTask (name, prereqs, action, opts)](#apidoc.element.jake.FileTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.Namespace)
1.  [function <span class="apidocSignatureSpan">jake.</span>PackageTask ()](#apidoc.element.jake.PackageTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>PublishTask ()](#apidoc.element.jake.PublishTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>Rule (opts)](#apidoc.element.jake.Rule)
1.  [function <span class="apidocSignatureSpan">jake.</span>SortedCollection (d)](#apidoc.element.jake.SortedCollection)
1.  [function <span class="apidocSignatureSpan">jake.</span>Task ()](#apidoc.element.jake.Task)
1.  [function <span class="apidocSignatureSpan">jake.</span>TestTask ()](#apidoc.element.jake.TestTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>WatchTask ()](#apidoc.element.jake.WatchTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>absolutize (p)](#apidoc.element.jake.absolutize)
1.  [function <span class="apidocSignatureSpan">jake.</span>async.AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.</span>async.AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup)
1.  [function <span class="apidocSignatureSpan">jake.</span>async.Initializer (steps, callback)](#apidoc.element.jake.async.Initializer)
1.  [function <span class="apidocSignatureSpan">jake.</span>async.SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.</span>attemptRule (name, ns, level)](#apidoc.element.jake.attemptRule)
1.  [function <span class="apidocSignatureSpan">jake.</span>basedir (pathParam)](#apidoc.element.jake.basedir)
1.  [function <span class="apidocSignatureSpan">jake.</span>bind ()](#apidoc.element.jake.bind)
1.  [function <span class="apidocSignatureSpan">jake.</span>complete (task, val)](#apidoc.element.jake.complete)
1.  [function <span class="apidocSignatureSpan">jake.</span>cpR (fromPath, toPath, options)](#apidoc.element.jake.cpR)
1.  [function <span class="apidocSignatureSpan">jake.</span>createExec (a, b, c)](#apidoc.element.jake.createExec)
1.  [function <span class="apidocSignatureSpan">jake.</span>createPlaceholderFileTask (name, namespace)](#apidoc.element.jake.createPlaceholderFileTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>createTask ()](#apidoc.element.jake.createTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>desc (description)](#apidoc.element.jake.desc)
1.  [function <span class="apidocSignatureSpan">jake.</span>directory (name)](#apidoc.element.jake.directory)
1.  [function <span class="apidocSignatureSpan">jake.</span>enhance ()](#apidoc.element.jake.enhance)
1.  [function <span class="apidocSignatureSpan">jake.</span>exec (a, b, c)](#apidoc.element.jake.exec)
1.  [function <span class="apidocSignatureSpan">jake.</span>exists (path, callback)](#apidoc.element.jake.exists)
1.  [function <span class="apidocSignatureSpan">jake.</span>existsSync (path)](#apidoc.element.jake.existsSync)
1.  [function <span class="apidocSignatureSpan">jake.</span>fail (err, code)](#apidoc.element.jake.fail)
1.  [function <span class="apidocSignatureSpan">jake.</span>file (name, prereqs, action, opts)](#apidoc.element.jake.file)
1.  [function <span class="apidocSignatureSpan">jake.</span>init ()](#apidoc.element.jake.init)
1.  [function <span class="apidocSignatureSpan">jake.</span>isAbsolute (p)](#apidoc.element.jake.isAbsolute)
1.  [function <span class="apidocSignatureSpan">jake.</span>isEmpty (val)](#apidoc.element.jake.isEmpty)
1.  [function <span class="apidocSignatureSpan">jake.</span>log (obj)](#apidoc.element.jake.log)
1.  [function <span class="apidocSignatureSpan">jake.</span>mixin ()](#apidoc.element.jake.mixin)
1.  [function <span class="apidocSignatureSpan">jake.</span>mkdirP (dir, mode)](#apidoc.element.jake.mkdirP)
1.  [function <span class="apidocSignatureSpan">jake.</span>namespace (name, closure)](#apidoc.element.jake.namespace)
1.  [function <span class="apidocSignatureSpan">jake.</span>npmPublishTask (name, prereqs, opts, definition)](#apidoc.element.jake.npmPublishTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>packageTask (name, version, definition)](#apidoc.element.jake.packageTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>parseAllTasks ()](#apidoc.element.jake.parseAllTasks)
1.  [function <span class="apidocSignatureSpan">jake.</span>publishTask (name, prereqs, opts, definition)](#apidoc.element.jake.publishTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>readdirR (dir, opts)](#apidoc.element.jake.readdirR)
1.  [function <span class="apidocSignatureSpan">jake.</span>request (opts, callback)](#apidoc.element.jake.request)
1.  [function <span class="apidocSignatureSpan">jake.</span>requireLocal (module, message)](#apidoc.element.jake.requireLocal)
1.  [function <span class="apidocSignatureSpan">jake.</span>rmRf (p, options)](#apidoc.element.jake.rmRf)
1.  [function <span class="apidocSignatureSpan">jake.</span>rule ()](#apidoc.element.jake.rule)
1.  [function <span class="apidocSignatureSpan">jake.</span>run ()](#apidoc.element.jake.run)
1.  [function <span class="apidocSignatureSpan">jake.</span>searchParentPath (location, beginPath, callback)](#apidoc.element.jake.searchParentPath)
1.  [function <span class="apidocSignatureSpan">jake.</span>showAllTaskDescriptions (f)](#apidoc.element.jake.showAllTaskDescriptions)
1.  [function <span class="apidocSignatureSpan">jake.</span>task (name, prereqs, action, opts)](#apidoc.element.jake.task)
1.  [function <span class="apidocSignatureSpan">jake.</span>testTask ()](#apidoc.element.jake.testTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>watch ()](#apidoc.element.jake.watch)
1.  [function <span class="apidocSignatureSpan">jake.</span>watchTask (name, taskNames, definition)](#apidoc.element.jake.watchTask)
1.  number <span class="apidocSignatureSpan">jake.</span>_eventsCount
1.  object <span class="apidocSignatureSpan">jake.</span>DirectoryTask.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>EventBuffer.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>Exec.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>FileList.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>FileTask.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>Namespace.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>PackageTask.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>PublishTask.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>Rule.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>SortedCollection.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>Task.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>XML
1.  object <span class="apidocSignatureSpan">jake.</span>_events
1.  object <span class="apidocSignatureSpan">jake.</span>_invocationChain
1.  object <span class="apidocSignatureSpan">jake.</span>api
1.  object <span class="apidocSignatureSpan">jake.</span>array
1.  object <span class="apidocSignatureSpan">jake.</span>async
1.  object <span class="apidocSignatureSpan">jake.</span>async.AsyncChain.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>async.AsyncGroup.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>async.Initializer.prototype
1.  object <span class="apidocSignatureSpan">jake.</span>currentNamespace
1.  object <span class="apidocSignatureSpan">jake.</span>currentTaskDescription
1.  object <span class="apidocSignatureSpan">jake.</span>date
1.  object <span class="apidocSignatureSpan">jake.</span>date.supportedFormats
1.  object <span class="apidocSignatureSpan">jake.</span>defaultNamespace
1.  object <span class="apidocSignatureSpan">jake.</span>domain
1.  object <span class="apidocSignatureSpan">jake.</span>i18n
1.  object <span class="apidocSignatureSpan">jake.</span>inflection
1.  object <span class="apidocSignatureSpan">jake.</span>loader
1.  object <span class="apidocSignatureSpan">jake.</span>logger
1.  object <span class="apidocSignatureSpan">jake.</span>network
1.  object <span class="apidocSignatureSpan">jake.</span>object
1.  object <span class="apidocSignatureSpan">jake.</span>package_task
1.  object <span class="apidocSignatureSpan">jake.</span>parseargs
1.  object <span class="apidocSignatureSpan">jake.</span>program
1.  object <span class="apidocSignatureSpan">jake.</span>publish_task
1.  object <span class="apidocSignatureSpan">jake.</span>string
1.  object <span class="apidocSignatureSpan">jake.</span>uri
1.  object <span class="apidocSignatureSpan">jake.</span>watch_task
1.  string <span class="apidocSignatureSpan">jake.</span>version

#### [module jake.DirectoryTask](#apidoc.module.jake.DirectoryTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>DirectoryTask (name)](#apidoc.element.jake.DirectoryTask.DirectoryTask)

#### [module jake.DirectoryTask.prototype](#apidoc.module.jake.DirectoryTask.prototype)
1.  boolean <span class="apidocSignatureSpan">jake.DirectoryTask.prototype.</span>dummy
1.  [function <span class="apidocSignatureSpan">jake.DirectoryTask.prototype.</span>constructor (name)](#apidoc.element.jake.DirectoryTask.prototype.constructor)
1.  object <span class="apidocSignatureSpan">jake.DirectoryTask.prototype.</span>modTime

#### [module jake.EventBuffer](#apidoc.module.jake.EventBuffer)
1.  [function <span class="apidocSignatureSpan">jake.</span>EventBuffer (src, events)](#apidoc.element.jake.EventBuffer.EventBuffer)

#### [module jake.EventBuffer.prototype](#apidoc.module.jake.EventBuffer.prototype)
1.  [function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>constructor (src, events)](#apidoc.element.jake.EventBuffer.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>emit (name, args)](#apidoc.element.jake.EventBuffer.prototype.emit)
1.  [function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>proxyEmit (name, args)](#apidoc.element.jake.EventBuffer.prototype.proxyEmit)
1.  [function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>sync (outlet)](#apidoc.element.jake.EventBuffer.prototype.sync)

#### [module jake.Exec](#apidoc.module.jake.Exec)
1.  [function <span class="apidocSignatureSpan">jake.</span>Exec ()](#apidoc.element.jake.Exec.Exec)
1.  [function <span class="apidocSignatureSpan">jake.Exec.</span>super_ ()](#apidoc.element.jake.Exec.super_)

#### [module jake.Exec.prototype](#apidoc.module.jake.Exec.prototype)
1.  [function <span class="apidocSignatureSpan">jake.Exec.prototype.</span>append (cmd)](#apidoc.element.jake.Exec.prototype.append)
1.  [function <span class="apidocSignatureSpan">jake.Exec.prototype.</span>run ()](#apidoc.element.jake.Exec.prototype.run)

#### [module jake.FileList](#apidoc.module.jake.FileList)
1.  [function <span class="apidocSignatureSpan">jake.</span>FileList ()](#apidoc.element.jake.FileList.FileList)
1.  [function <span class="apidocSignatureSpan">jake.FileList.</span>clone (list, items)](#apidoc.element.jake.FileList.clone)

#### [module jake.FileList.prototype](#apidoc.module.jake.FileList.prototype)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>clearExclusions ()](#apidoc.element.jake.FileList.prototype.clearExclusions)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>clearInclusions ()](#apidoc.element.jake.FileList.prototype.clearInclusions)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>exclude ()](#apidoc.element.jake.FileList.prototype.exclude)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>include (items)](#apidoc.element.jake.FileList.prototype.include)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>resolve ()](#apidoc.element.jake.FileList.prototype.resolve)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>shouldExclude (name)](#apidoc.element.jake.FileList.prototype.shouldExclude)
1.  [function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>toArray ()](#apidoc.element.jake.FileList.prototype.toArray)

#### [module jake.FileTask](#apidoc.module.jake.FileTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>FileTask (name, prereqs, action, opts)](#apidoc.element.jake.FileTask.FileTask)

#### [module jake.FileTask.prototype](#apidoc.module.jake.FileTask.prototype)
1.  [function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>complete ()](#apidoc.element.jake.FileTask.prototype.complete)
1.  [function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>constructor (name, prereqs, action, opts)](#apidoc.element.jake.FileTask.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>isNeeded ()](#apidoc.element.jake.FileTask.prototype.isNeeded)
1.  [function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>updateModTime ()](#apidoc.element.jake.FileTask.prototype.updateModTime)

#### [module jake.Namespace](#apidoc.module.jake.Namespace)
1.  [function <span class="apidocSignatureSpan">jake.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.Namespace.Namespace)

#### [module jake.Namespace.prototype](#apidoc.module.jake.Namespace.prototype)
1.  [function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>getPath ()](#apidoc.element.jake.Namespace.prototype.getPath)
1.  [function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>matchRule (relativeName)](#apidoc.element.jake.Namespace.prototype.matchRule)
1.  [function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>resolveNamespace (relativeName)](#apidoc.element.jake.Namespace.prototype.resolveNamespace)
1.  [function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>resolveTask (relativeName)](#apidoc.element.jake.Namespace.prototype.resolveTask)

#### [module jake.PackageTask](#apidoc.module.jake.PackageTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>PackageTask ()](#apidoc.element.jake.PackageTask.PackageTask)

#### [module jake.PackageTask.prototype](#apidoc.module.jake.PackageTask.prototype)
1.  [function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>define ()](#apidoc.element.jake.PackageTask.prototype.define)
1.  [function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>packageDirPath ()](#apidoc.element.jake.PackageTask.prototype.packageDirPath)
1.  [function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>packageName ()](#apidoc.element.jake.PackageTask.prototype.packageName)

#### [module jake.PublishTask](#apidoc.module.jake.PublishTask)
1.  [function <span class="apidocSignatureSpan">jake.</span>PublishTask ()](#apidoc.element.jake.PublishTask.PublishTask)

#### [module jake.PublishTask.prototype](#apidoc.module.jake.PublishTask.prototype)
1.  [function <span class="apidocSignatureSpan">jake.PublishTask.prototype.</span>define ()](#apidoc.element.jake.PublishTask.prototype.define)

#### [module jake.Rule](#apidoc.module.jake.Rule)
1.  [function <span class="apidocSignatureSpan">jake.</span>Rule (opts)](#apidoc.element.jake.Rule.Rule)

#### [module jake.Rule.prototype](#apidoc.module.jake.Rule.prototype)
1.  [function <span class="apidocSignatureSpan">jake.Rule.prototype.</span>createTask (fullName, level)](#apidoc.element.jake.Rule.prototype.createTask)
1.  [function <span class="apidocSignatureSpan">jake.Rule.prototype.</span>match (name)](#apidoc.element.jake.Rule.prototype.match)

#### [module jake.SortedCollection](#apidoc.module.jake.SortedCollection)
1.  [function <span class="apidocSignatureSpan">jake.</span>SortedCollection (d)](#apidoc.element.jake.SortedCollection.SortedCollection)

#### [module jake.SortedCollection.prototype](#apidoc.module.jake.SortedCollection.prototype)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>addItem (key, val)](#apidoc.element.jake.SortedCollection.prototype.addItem)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>allKeys (str)](#apidoc.element.jake.SortedCollection.prototype.allKeys)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>clone ()](#apidoc.element.jake.SortedCollection.prototype.clone)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>concat (hNew)](#apidoc.element.jake.SortedCollection.prototype.concat)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>each (func, opts)](#apidoc.element.jake.SortedCollection.prototype.each)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>eachKey (func)](#apidoc.element.jake.SortedCollection.prototype.eachKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>eachValue (func)](#apidoc.element.jake.SortedCollection.prototype.eachValue)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getByIndex (ind)](#apidoc.element.jake.SortedCollection.prototype.getByIndex)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getByKey (key)](#apidoc.element.jake.SortedCollection.prototype.getByKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getItem (p)](#apidoc.element.jake.SortedCollection.prototype.getItem)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getPosition (key)](#apidoc.element.jake.SortedCollection.prototype.getPosition)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>hasKey (key)](#apidoc.element.jake.SortedCollection.prototype.hasKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>hasValue (val)](#apidoc.element.jake.SortedCollection.prototype.hasValue)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>insertAfterKey (refKey, key, val)](#apidoc.element.jake.SortedCollection.prototype.insertAfterKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>insertAtIndex (ind, key, val)](#apidoc.element.jake.SortedCollection.prototype.insertAtIndex)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>pop ()](#apidoc.element.jake.SortedCollection.prototype.pop)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>push (key, val)](#apidoc.element.jake.SortedCollection.prototype.push)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeByIndex (ind)](#apidoc.element.jake.SortedCollection.prototype.removeByIndex)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeByKey (key)](#apidoc.element.jake.SortedCollection.prototype.removeByKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeItem (p)](#apidoc.element.jake.SortedCollection.prototype.removeItem)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>replaceKey (oldKey, newKey)](#apidoc.element.jake.SortedCollection.prototype.replaceKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>reverse ()](#apidoc.element.jake.SortedCollection.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setByIndex (ind, val)](#apidoc.element.jake.SortedCollection.prototype.setByIndex)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setByKey (key, val)](#apidoc.element.jake.SortedCollection.prototype.setByKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setItem (p, val)](#apidoc.element.jake.SortedCollection.prototype.setItem)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>shift ()](#apidoc.element.jake.SortedCollection.prototype.shift)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>sort (c)](#apidoc.element.jake.SortedCollection.prototype.sort)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>sortByKey (comp)](#apidoc.element.jake.SortedCollection.prototype.sortByKey)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>splice (index, numToRemove, hash)](#apidoc.element.jake.SortedCollection.prototype.splice)
1.  [function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>unshift (key, val)](#apidoc.element.jake.SortedCollection.prototype.unshift)

#### [module jake.Task](#apidoc.module.jake.Task)
1.  [function <span class="apidocSignatureSpan">jake.</span>Task ()](#apidoc.element.jake.Task.Task)
1.  [function <span class="apidocSignatureSpan">jake.Task.</span>getBaseNamespacePath (fullName)](#apidoc.element.jake.Task.getBaseNamespacePath)
1.  [function <span class="apidocSignatureSpan">jake.Task.</span>getBaseTaskName (fullName)](#apidoc.element.jake.Task.getBaseTaskName)
1.  [function <span class="apidocSignatureSpan">jake.Task.</span>super_ ()](#apidoc.element.jake.Task.super_)
1.  object <span class="apidocSignatureSpan">jake.Task.</span>runStatuses

#### [module jake.Task.prototype](#apidoc.module.jake.Task.prototype)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>complete (val)](#apidoc.element.jake.Task.prototype.complete)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>execute ()](#apidoc.element.jake.Task.prototype.execute)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>handlePrereqComplete (prereq)](#apidoc.element.jake.Task.prototype.handlePrereqComplete)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>init (name, prereqs, action, options)](#apidoc.element.jake.Task.prototype.init)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>invoke ()](#apidoc.element.jake.Task.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>isNeeded ()](#apidoc.element.jake.Task.prototype.isNeeded)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>nextPrereq ()](#apidoc.element.jake.Task.prototype.nextPrereq)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>reenable (deep)](#apidoc.element.jake.Task.prototype.reenable)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>run ()](#apidoc.element.jake.Task.prototype.run)
1.  [function <span class="apidocSignatureSpan">jake.Task.prototype.</span>runPrereqs ()](#apidoc.element.jake.Task.prototype.runPrereqs)

#### [module jake.XML](#apidoc.module.jake.XML)
1.  [function <span class="apidocSignatureSpan">jake.XML.</span>setIndentLevel (level)](#apidoc.element.jake.XML.setIndentLevel)
1.  [function <span class="apidocSignatureSpan">jake.XML.</span>stringify (obj, opts)](#apidoc.element.jake.XML.stringify)
1.  object <span class="apidocSignatureSpan">jake.XML.</span>config

#### [module jake.api](#apidoc.module.jake.api)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>complete (task, val)](#apidoc.element.jake.api.complete)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>desc (description)](#apidoc.element.jake.api.desc)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>directory (name)](#apidoc.element.jake.api.directory)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>fail (err, code)](#apidoc.element.jake.api.fail)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>file (name, prereqs, action, opts)](#apidoc.element.jake.api.file)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>namespace (name, closure)](#apidoc.element.jake.api.namespace)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>npmPublishTask (name, prereqs, opts, definition)](#apidoc.element.jake.api.npmPublishTask)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>packageTask (name, version, definition)](#apidoc.element.jake.api.packageTask)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>publishTask (name, prereqs, opts, definition)](#apidoc.element.jake.api.publishTask)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>rule ()](#apidoc.element.jake.api.rule)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>task (name, prereqs, action, opts)](#apidoc.element.jake.api.task)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>testTask ()](#apidoc.element.jake.api.testTask)
1.  [function <span class="apidocSignatureSpan">jake.api.</span>watchTask (name, taskNames, definition)](#apidoc.element.jake.api.watchTask)

#### [module jake.array](#apidoc.module.jake.array)
1.  [function <span class="apidocSignatureSpan">jake.array.</span>humanize (a)](#apidoc.element.jake.array.humanize)
1.  [function <span class="apidocSignatureSpan">jake.array.</span>include (array, item)](#apidoc.element.jake.array.include)
1.  [function <span class="apidocSignatureSpan">jake.array.</span>included (item, array)](#apidoc.element.jake.array.included)

#### [module jake.async](#apidoc.module.jake.async)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>AsyncCall (func, args, callback, context)](#apidoc.element.jake.async.AsyncCall)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>Initializer (steps, callback)](#apidoc.element.jake.async.Initializer)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>execNonBlocking (func)](#apidoc.element.jake.async.execNonBlocking)
1.  object <span class="apidocSignatureSpan">jake.async.</span>AsyncBase

#### [module jake.async.AsyncChain](#apidoc.module.jake.async.AsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain.AsyncChain)

#### [module jake.async.AsyncChain.prototype](#apidoc.module.jake.async.AsyncChain.prototype)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>abort ()](#apidoc.element.jake.async.AsyncChain.prototype.abort)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>addItem (item)](#apidoc.element.jake.async.AsyncChain.prototype.addItem)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>execCallback ()](#apidoc.element.jake.async.AsyncChain.prototype.execCallback)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>init (chain)](#apidoc.element.jake.async.AsyncChain.prototype.init)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>last ()](#apidoc.element.jake.async.AsyncChain.prototype.last)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>next ()](#apidoc.element.jake.async.AsyncChain.prototype.next)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>push (item)](#apidoc.element.jake.async.AsyncChain.prototype.push)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>run ()](#apidoc.element.jake.async.AsyncChain.prototype.run)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>runItem (item)](#apidoc.element.jake.async.AsyncChain.prototype.runItem)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>shortCircuit ()](#apidoc.element.jake.async.AsyncChain.prototype.shortCircuit)

#### [module jake.async.AsyncGroup](#apidoc.module.jake.async.AsyncGroup)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup.AsyncGroup)

#### [module jake.async.AsyncGroup.prototype](#apidoc.module.jake.async.AsyncGroup.prototype)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>finish ()](#apidoc.element.jake.async.AsyncGroup.prototype.finish)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>last ()](#apidoc.element.jake.async.AsyncGroup.prototype.last)
1.  [function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>run ()](#apidoc.element.jake.async.AsyncGroup.prototype.run)

#### [module jake.async.Initializer](#apidoc.module.jake.async.Initializer)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>Initializer (steps, callback)](#apidoc.element.jake.async.Initializer.Initializer)

#### [module jake.async.Initializer.prototype](#apidoc.module.jake.async.Initializer.prototype)
1.  [function <span class="apidocSignatureSpan">jake.async.Initializer.prototype.</span>complete (step)](#apidoc.element.jake.async.Initializer.prototype.complete)

#### [module jake.async.SimpleAsyncChain](#apidoc.module.jake.async.SimpleAsyncChain)
1.  [function <span class="apidocSignatureSpan">jake.async.</span>SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain.SimpleAsyncChain)

#### [module jake.date](#apidoc.module.jake.date)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>add (dt, interv, incr)](#apidoc.element.jake.date.add)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>calcCentury (year)](#apidoc.element.jake.date.calcCentury)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>calcDays (dt)](#apidoc.element.jake.date.calcDays)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>convertOneBase (d)](#apidoc.element.jake.date.convertOneBase)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>diff (date1, date2, interv)](#apidoc.element.jake.date.diff)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>getMeridian (h)](#apidoc.element.jake.date.getMeridian)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>getMeridiem (h)](#apidoc.element.jake.date.getMeridiem)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>getSupportedFormats ()](#apidoc.element.jake.date.getSupportedFormats)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>getTwoDigitYear (yr)](#apidoc.element.jake.date.getTwoDigitYear)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>hrMil2Std (hour)](#apidoc.element.jake.date.hrMil2Std)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>hrStd2Mil (hour, pm)](#apidoc.element.jake.date.hrStd2Mil)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>parse (val, options)](#apidoc.element.jake.date.parse)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>relativeTime (dt, options)](#apidoc.element.jake.date.relativeTime)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>strftime (dt, format)](#apidoc.element.jake.date.strftime)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>strftimeNotImplemented (s)](#apidoc.element.jake.date.strftimeNotImplemented)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>toISO8601 (dt, options)](#apidoc.element.jake.date.toISO8601)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>toIso8601 (dt, options)](#apidoc.element.jake.date.toIso8601)
1.  [function <span class="apidocSignatureSpan">jake.date.</span>toUTC (dt)](#apidoc.element.jake.date.toUTC)
1.  object <span class="apidocSignatureSpan">jake.date.</span>dateParts
1.  object <span class="apidocSignatureSpan">jake.date.</span>meridian
1.  object <span class="apidocSignatureSpan">jake.date.</span>meridiem
1.  object <span class="apidocSignatureSpan">jake.date.</span>monthLong
1.  object <span class="apidocSignatureSpan">jake.date.</span>monthShort
1.  object <span class="apidocSignatureSpan">jake.date.</span>supportedFormats
1.  object <span class="apidocSignatureSpan">jake.date.</span>supportedFormatsPat
1.  object <span class="apidocSignatureSpan">jake.date.</span>weekdayLong
1.  object <span class="apidocSignatureSpan">jake.date.</span>weekdayShort

#### [module jake.date.supportedFormats](#apidoc.module.jake.date.supportedFormats)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>A (dt)](#apidoc.element.jake.date.supportedFormats.A)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>B (dt)](#apidoc.element.jake.date.supportedFormats.B)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>C (dt)](#apidoc.element.jake.date.supportedFormats.C)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>D (dt)](#apidoc.element.jake.date.supportedFormats.D)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>F (dt)](#apidoc.element.jake.date.supportedFormats.F)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>G ()](#apidoc.element.jake.date.supportedFormats.G)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>H (dt)](#apidoc.element.jake.date.supportedFormats.H)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>I (dt)](#apidoc.element.jake.date.supportedFormats.I)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>M (dt)](#apidoc.element.jake.date.supportedFormats.M)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>R (dt)](#apidoc.element.jake.date.supportedFormats.R)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>S (dt)](#apidoc.element.jake.date.supportedFormats.S)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>T (dt)](#apidoc.element.jake.date.supportedFormats.T)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>U ()](#apidoc.element.jake.date.supportedFormats.U)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>V ()](#apidoc.element.jake.date.supportedFormats.V)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>W ()](#apidoc.element.jake.date.supportedFormats.W)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>X (dt)](#apidoc.element.jake.date.supportedFormats.X)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>Y (dt)](#apidoc.element.jake.date.supportedFormats.Y)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>Z ()](#apidoc.element.jake.date.supportedFormats.Z)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>a (dt)](#apidoc.element.jake.date.supportedFormats.a)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>b (dt)](#apidoc.element.jake.date.supportedFormats.b)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>c (dt)](#apidoc.element.jake.date.supportedFormats.c)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>d (dt)](#apidoc.element.jake.date.supportedFormats.d)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>e (dt)](#apidoc.element.jake.date.supportedFormats.e)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>f ()](#apidoc.element.jake.date.supportedFormats.f)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>g ()](#apidoc.element.jake.date.supportedFormats.g)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>h (dt)](#apidoc.element.jake.date.supportedFormats.h)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>j (dt)](#apidoc.element.jake.date.supportedFormats.j)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>k (dt)](#apidoc.element.jake.date.supportedFormats.k)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>l (dt)](#apidoc.element.jake.date.supportedFormats.l)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>m (dt)](#apidoc.element.jake.date.supportedFormats.m)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>n ()](#apidoc.element.jake.date.supportedFormats.n)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>p (dt)](#apidoc.element.jake.date.supportedFormats.p)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>r (dt)](#apidoc.element.jake.date.supportedFormats.r)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>t ()](#apidoc.element.jake.date.supportedFormats.t)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>u (dt)](#apidoc.element.jake.date.supportedFormats.u)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>w (dt)](#apidoc.element.jake.date.supportedFormats.w)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>x (dt)](#apidoc.element.jake.date.supportedFormats.x)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>y (dt)](#apidoc.element.jake.date.supportedFormats.y)
1.  [function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>z ()](#apidoc.element.jake.date.supportedFormats.z)

#### [module jake.i18n](#apidoc.module.jake.i18n)
1.  [function <span class="apidocSignatureSpan">jake.i18n.</span>I18n (locale)](#apidoc.element.jake.i18n.I18n)
1.  [function <span class="apidocSignatureSpan">jake.i18n.</span>getDefaultLocale ()](#apidoc.element.jake.i18n.getDefaultLocale)
1.  [function <span class="apidocSignatureSpan">jake.i18n.</span>getText (key, opts, locale)](#apidoc.element.jake.i18n.getText)
1.  [function <span class="apidocSignatureSpan">jake.i18n.</span>loadLocale (locale, strings)](#apidoc.element.jake.i18n.loadLocale)
1.  [function <span class="apidocSignatureSpan">jake.i18n.</span>setDefaultLocale (locale)](#apidoc.element.jake.i18n.setDefaultLocale)

#### [module jake.inflection](#apidoc.module.jake.inflection)
1.  [function <span class="apidocSignatureSpan">jake.inflection.</span>parse (type, word)](#apidoc.element.jake.inflection.parse)
1.  [function <span class="apidocSignatureSpan">jake.inflection.</span>pluralize (word)](#apidoc.element.jake.inflection.pluralize)
1.  [function <span class="apidocSignatureSpan">jake.inflection.</span>singularize (word)](#apidoc.element.jake.inflection.singularize)
1.  object <span class="apidocSignatureSpan">jake.inflection.</span>inflections

#### [module jake.loader](#apidoc.module.jake.loader)
1.  [function <span class="apidocSignatureSpan">jake.loader.</span>loadDirectory (d)](#apidoc.element.jake.loader.loadDirectory)
1.  [function <span class="apidocSignatureSpan">jake.loader.</span>loadFile (file)](#apidoc.element.jake.loader.loadFile)

#### [module jake.log](#apidoc.module.jake.log)
1.  [function <span class="apidocSignatureSpan">jake.</span>log (obj)](#apidoc.element.jake.log.log)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>access (obj)](#apidoc.element.jake.log.access)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>alert (obj)](#apidoc.element.jake.log.alert)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>critical (obj)](#apidoc.element.jake.log.critical)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>debug (obj)](#apidoc.element.jake.log.debug)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>emergency (obj)](#apidoc.element.jake.log.emergency)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>error (obj)](#apidoc.element.jake.log.error)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>info (obj)](#apidoc.element.jake.log.info)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>notice (obj)](#apidoc.element.jake.log.notice)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>registerLogger (logger)](#apidoc.element.jake.log.registerLogger)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>warn (obj)](#apidoc.element.jake.log.warn)
1.  [function <span class="apidocSignatureSpan">jake.log.</span>warning (obj)](#apidoc.element.jake.log.warning)

#### [module jake.logger](#apidoc.module.jake.logger)
1.  [function <span class="apidocSignatureSpan">jake.logger.</span>error (out)](#apidoc.element.jake.logger.error)
1.  [function <span class="apidocSignatureSpan">jake.logger.</span>log (out)](#apidoc.element.jake.logger.log)

#### [module jake.namespace](#apidoc.module.jake.namespace)
1.  [function <span class="apidocSignatureSpan">jake.namespace.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.namespace.Namespace)

#### [module jake.network](#apidoc.module.jake.network)
1.  [function <span class="apidocSignatureSpan">jake.network.</span>isPortOpen (port, host, callback)](#apidoc.element.jake.network.isPortOpen)

#### [module jake.object](#apidoc.module.jake.object)
1.  [function <span class="apidocSignatureSpan">jake.object.</span>isEmpty (object)](#apidoc.element.jake.object.isEmpty)
1.  [function <span class="apidocSignatureSpan">jake.object.</span>merge (object, otherObject)](#apidoc.element.jake.object.merge)
1.  [function <span class="apidocSignatureSpan">jake.object.</span>reverseMerge (object, defaultObject)](#apidoc.element.jake.object.reverseMerge)
1.  [function <span class="apidocSignatureSpan">jake.object.</span>toArray (object)](#apidoc.element.jake.object.toArray)

#### [module jake.package_task](#apidoc.module.jake.package_task)
1.  [function <span class="apidocSignatureSpan">jake.package_task.</span>PackageTask ()](#apidoc.element.jake.package_task.PackageTask)

#### [module jake.parseargs](#apidoc.module.jake.parseargs)
1.  [function <span class="apidocSignatureSpan">jake.parseargs.</span>Parser (opts)](#apidoc.element.jake.parseargs.Parser)

#### [module jake.program](#apidoc.module.jake.program)
1.  [function <span class="apidocSignatureSpan">jake.program.</span>Program ()](#apidoc.element.jake.program.Program)

#### [module jake.publish_task](#apidoc.module.jake.publish_task)
1.  [function <span class="apidocSignatureSpan">jake.publish_task.</span>PublishTask ()](#apidoc.element.jake.publish_task.PublishTask)

#### [module jake.rule](#apidoc.module.jake.rule)
1.  [function <span class="apidocSignatureSpan">jake.rule.</span>Rule (opts)](#apidoc.element.jake.rule.Rule)
1.  object <span class="apidocSignatureSpan">jake.rule.</span>Matcher

#### [module jake.string](#apidoc.module.jake.string)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>camelize (string, options)](#apidoc.element.jake.string.camelize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>capitalize (string)](#apidoc.element.jake.string.capitalize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>chomp (string, character)](#apidoc.element.jake.string.chomp)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>chop (string)](#apidoc.element.jake.string.chop)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>dasherize (string, replace)](#apidoc.element.jake.string.dasherize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>decamelize (string, separ)](#apidoc.element.jake.string.decamelize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>decapitalize (string)](#apidoc.element.jake.string.decapitalize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>escapeRegExpChars (string)](#apidoc.element.jake.string.escapeRegExpChars)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>escapeXML (str)](#apidoc.element.jake.string.escapeXML)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>getInflection (name, key, pluralization)](#apidoc.element.jake.string.getInflection)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>getInflections (name)](#apidoc.element.jake.string.getInflections)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>include (searchIn, searchFor)](#apidoc.element.jake.string.include)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>lpad (string, character, width)](#apidoc.element.jake.string.lpad)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>ltrim (string, character)](#apidoc.element.jake.string.ltrim)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>needsEscape (string)](#apidoc.element.jake.string.needsEscape)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>needsUnescape (string)](#apidoc.element.jake.string.needsUnescape)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>nl2br (string)](#apidoc.element.jake.string.nl2br)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>pad (string, character, width)](#apidoc.element.jake.string.pad)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>reverse (string)](#apidoc.element.jake.string.reverse)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>rpad (string, character, width)](#apidoc.element.jake.string.rpad)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>rtrim (string, character)](#apidoc.element.jake.string.rtrim)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>snakeize (string, separ)](#apidoc.element.jake.string.snakeize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>stripTags (string, allowed)](#apidoc.element.jake.string.stripTags)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>toArray (string)](#apidoc.element.jake.string.toArray)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>trim (string, character)](#apidoc.element.jake.string.trim)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>truncate (string, options, callback)](#apidoc.element.jake.string.truncate)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>truncateHTML (string, options, callback)](#apidoc.element.jake.string.truncateHTML)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>underscoreize (string, separ)](#apidoc.element.jake.string.underscoreize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>underscorize (string, separ)](#apidoc.element.jake.string.underscorize)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>unescapeXML (str)](#apidoc.element.jake.string.unescapeXML)
1.  [function <span class="apidocSignatureSpan">jake.string.</span>uuid (length, radix)](#apidoc.element.jake.string.uuid)

#### [module jake.uri](#apidoc.module.jake.uri)
1.  [function <span class="apidocSignatureSpan">jake.uri.</span>getFileExtension (path)](#apidoc.element.jake.uri.getFileExtension)
1.  [function <span class="apidocSignatureSpan">jake.uri.</span>objectify (str, o)](#apidoc.element.jake.uri.objectify)
1.  [function <span class="apidocSignatureSpan">jake.uri.</span>paramify (obj, o)](#apidoc.element.jake.uri.paramify)

#### [module jake.watch_task](#apidoc.module.jake.watch_task)
1.  [function <span class="apidocSignatureSpan">jake.watch_task.</span>WatchTask ()](#apidoc.element.jake.watch_task.WatchTask)



# <a name="apidoc.module.jake"></a>[module jake](#apidoc.module.jake)

#### <a name="apidoc.element.jake.DirectoryTask"></a>[function <span class="apidocSignatureSpan">jake.</span>DirectoryTask (name)](#apidoc.element.jake.DirectoryTask)
- description and source-code
```javascript
DirectoryTask = function (name) {
  this.modTime = null;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.EventBuffer"></a>[function <span class="apidocSignatureSpan">jake.</span>EventBuffer (src, events)](#apidoc.element.jake.EventBuffer)
- description and source-code
```javascript
EventBuffer = function (src, events) {
  // By default, we service the default stream events
  var self = this
    , streamEvents = ['data', 'end', 'error', 'close', 'fd', 'drain', 'pipe'];
  this.events = events || streamEvents;
  this.emitter = src;
  this.eventBuffer = [];
  this.outlet = null;
  this.events.forEach(function (name) {
    self.emitter.addListener(name, function () {
      self.proxyEmit(name, arguments);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Exec"></a>[function <span class="apidocSignatureSpan">jake.</span>Exec ()](#apidoc.element.jake.Exec)
- description and source-code
```javascript
Exec = function () {
  var parsed = parseArgs(arguments)
    , cmds = parsed.cmds
    , opts = parsed.opts
    , callback = parsed.callback;

  this._cmds = cmds;
  this._callback = callback;
  this._config = opts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileList"></a>[function <span class="apidocSignatureSpan">jake.</span>FileList ()](#apidoc.element.jake.FileList)
- description and source-code
```javascript
FileList = function () {
  var self = this
    , wrap;

  // List of glob-patterns or specific filenames
  this.pendingAdd = [];
  // Switched to false after lazy-eval of files
  this.pending = true;
  // Used to calculate exclusions from the list of files
  this.excludes = {
    pats: DEFAULT_IGNORE_PATTERNS.slice()
  , funcs: DEFAULT_IGNORE_FUNCS.slice()
  , regex: null
  };
  this.items = [];

  // Wrap the array methods with the delegates
  wrap = function (prop) {
    var arr;
    self[prop] = function () {
      if (self.pending) {
        self.resolve();
      }
      if (typeof self.items[prop] == 'function') {
        // Special method that return a copy
        if (SPECIAL_RETURN[prop]) {
          arr = self.items[prop].apply(self.items, arguments);
          return FileList.clone(self, arr);
        }
        else {
          return self.items[prop].apply(self.items, arguments);
        }
      }
      else {
        return self.items[prop];
      }
    };
  };
  for (var i = 0, ii = ARRAY_METHODS.length; i < ii; i++) {
    wrap(ARRAY_METHODS[i]);
  }

  // Include whatever files got passed to the constructor
  this.include.apply(this, arguments);

  // Fix constructor linkage
  this.constructor = FileList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileTask"></a>[function <span class="apidocSignatureSpan">jake.</span>FileTask (name, prereqs, action, opts)](#apidoc.element.jake.FileTask)
- description and source-code
```javascript
FileTask = function (name, prereqs, action, opts) {
  this.modTime = null;
  this.dummy = false;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Namespace"></a>[function <span class="apidocSignatureSpan">jake.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.Namespace)
- description and source-code
```javascript
Namespace = function (name, parentNamespace) {
  this.name = name;
  this.parentNamespace = parentNamespace;
  this.childNamespaces = {};
  this.tasks = {};
  this.rules = {};
  this.path = this.getPath();
}
```
- example usage
```shell
...
    task('clobber', function () {
      // Clobber the doc directory first
    });
  });
 */
this.namespace = function (name, closure) {
  var curr = jake.currentNamespace
    , ns = curr.childNamespaces[name] || new jake.Namespace(name, curr);
  curr.childNamespaces[name] = ns;
  jake.currentNamespace = ns;
  closure();
  jake.currentNamespace = curr;
  jake.currentTaskDescription = null;
  return ns;
};
...
```

#### <a name="apidoc.element.jake.PackageTask"></a>[function <span class="apidocSignatureSpan">jake.</span>PackageTask ()](#apidoc.element.jake.PackageTask)
- description and source-code
```javascript
PackageTask = function () {
  var args = Array.prototype.slice.call(arguments)
    , name = args.shift()
    , version = args.shift()
    , definition = args.pop()
    , prereqs = args.pop() || []; // Optional

    prereqs = [].concat(prereqs); // Accept string or list

<span class="apidocCodeCommentSpan">  /**
    @name jake.PackageTask#name
    @public
    @type {String}
    @description The name of the project
   */
</span>  this.name = name;
  /**
    @name jake.PackageTask#version
    @public
    @type {String}
    @description The project version-string
   */
  this.version = version;
  /**
    @name jake.PackageTask#prereqs
    @public
    @type {Array}
    @description Tasks to run before packaging
   */
  this.prereqs = prereqs;
  /**
    @name jake.PackageTask#version
    @public
    @type {String='pkg'}
    @description The directory-name to use for packaging the software
   */
  this.packageDir = 'pkg';
  /**
    @name jake.PackageTask#packageFiles
    @public
    @type {jake.FileList}
    @description The list of files and directories to include in the
    package-archive
   */
  this.packageFiles = new FileList();
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tgz archive of the package
   */
  this.needTar = false;
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tar.gz archive of the package
   */
  this.needTarGz = false;
  /**
    @name jake.PackageTask#needTarBz2
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a bzip2 .bz2 archive of the package
   */
  this.needTarBz2 = false;
  /**
    @name jake.PackageTask#needJar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'jar' utility to create
    a .jar archive of the package
   */
  this.needJar = false;
  /**
    @name jake.PackageTask#needZip
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'zip' utility to create
    a .zip archive of the package
   */
  this.needZip = false;
  /**
    @name jake.PackageTask#manifestFile
    @public
    @type {String=null}
    @description Can be set to point the 'jar' utility at a manifest
    file to use in a .jar archive. If unset, one will be automatically
    created by the 'jar' utility. This path should be relative to the
    root of the package directory (this.packageDir above, likely 'pkg')
   */
  this.manifestFile = null;
  /**
    @name jake.PackageTask#tarCommand
    @public
    @type {String='tar'}
    @description The shell-command to use for creating tar archives.
   */
  this.tarCommand = 'tar';
  /**
    @name jake.PackageTask#jarCommand
    @public
    @type {String='jar'}
    @description The shell-command to use for creating jar archives.
   */
  this.jarCommand = 'jar';
  /**
    @name jake.PackageTask#zipCommand
    @public
    @type {String='zip'}
    @description The shell-command to use for creating zip archives.
   */
  this.zipCommand = 'zip';
  /**
    @name jake.PackageTask#archiveNoBaseDir
    @public
    @type {Boolean=false}
    @description Simple option for performing the archive on the
    contents of the directory instead of the directory itself
   */
  this.archiveNoBaseDir = false;
  /**
    @name jake.PackageTask#archiveChangeDir
    @public
    @type {String=null}
    @description Equivalent to the '-C' command for the 'tar' and 'jar'
    commands. ("Change to this directory before adding files.")
   */
  this.archiveChangeDir = null;
  /**
    @name jake.PackageTask#archiveContentDir
    @public
    @type {String=null}
    @description Specifies the files and directories to include in the
    package-archive. If unset, this will default to the main package
    directory -- i.e., name + version.
   */
  this.archiveContentDir = null;

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
  }
  else {
    throw new Error();
  }
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
...
```

#### <a name="apidoc.element.jake.PublishTask"></a>[function <span class="apidocSignatureSpan">jake.</span>PublishTask ()](#apidoc.element.jake.PublishTask)
- description and source-code
```javascript
PublishTask = function () {
  var args = Array.prototype.slice.call(arguments).filter(function (item) {
        return typeof item != 'undefined';
      })
    , arg
    , opts = {}
    , definition
    , prereqs = []
    , createDef = function (arg) {
        return function () {
          this.packageFiles.include(arg);
        };
      };

  this.name = args.shift();

  // Old API, just name + list of files
  if (args.length == 1 && (Array.isArray(args[0]) || typeof args[0] == 'string')) {
    definition = createDef(args.pop());
  }
  // Current API, name + [prereqs] + [opts] + definition
  else {
    while ((arg = args.pop())) {
      // Definition func
      if (typeof arg == 'function') {
        definition = arg;
      }
      // Prereqs
      else if (Array.isArray(arg) || typeof arg == 'string') {
        prereqs = arg;
      }
      // Opts
      else {
        opts = arg;
      }
    }
  }

  this.prereqs = prereqs;
  this.packageFiles = new FileList();
  this.publishCmd = opts.publishCmd || 'npm publish %filename';
  this.publishMessage = opts.publishMessage || 'BOOM! Published.';
  this.gitCmd = opts.gitCmd || 'git';
  this.versionFiles = opts.versionFiles || ['package.json'];
  this.scheduleDelay = 5000;

  // Override utility funcs for testing
  this._ensureRepoClean = function (stdout) {
    if (stdout.length) {
      fail(new Error('Git repository is not clean.'));
    }
  };
  this._getCurrentBranch = function (stdout) {
    return utils.string.trim(stdout);
  };

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
this.npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};
...
```

#### <a name="apidoc.element.jake.Rule"></a>[function <span class="apidocSignatureSpan">jake.</span>Rule (opts)](#apidoc.element.jake.Rule)
- description and source-code
```javascript
Rule = function (opts) {
  this.pattern = opts.pattern;
  this.source = opts.source;
  this.prereqs = opts.prereqs;
  this.action = opts.action;
  this.opts = opts.opts;
  this.desc =  opts.desc;
  this.ns = opts.ns;
}
```
- example usage
```shell
...
    prereqs = arg;
  }
  else {
    opts = arg;
  }
}

jake.currentNamespace.rules[key] = new jake.Rule({
  pattern: pattern
, source: source
, prereqs: prereqs
, action: action
, opts: opts
, desc: jake.currentTaskDescription
, ns: jake.currentNamespace
...
```

#### <a name="apidoc.element.jake.SortedCollection"></a>[function <span class="apidocSignatureSpan">jake.</span>SortedCollection (d)](#apidoc.element.jake.SortedCollection)
- description and source-code
```javascript
SortedCollection = function (d) {
  this.count = 0;
  this.items = {}; // Hash keys and their values
  this.order = []; // Array for sort order
  if (d) {
    this.defaultValue = d;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task"></a>[function <span class="apidocSignatureSpan">jake.</span>Task ()](#apidoc.element.jake.Task)
- description and source-code
```javascript
Task = function () {
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.TestTask"></a>[function <span class="apidocSignatureSpan">jake.</span>TestTask ()](#apidoc.element.jake.TestTask)
- description and source-code
```javascript
TestTask = function () {
  var self = this
    , args = Array.prototype.slice.call(arguments)
    , name = args.shift()
    , definition = args.pop()
    , prereqs = args.pop() || [];

<span class="apidocCodeCommentSpan">  /**
    @name jake.TestTask#testNam
    @public
    @type {String}
    @description The name of the namespace to place the tests in, and
    the top-level task for running tests. Defaults to "test"
   */
</span>  this.testName = 'test';

  /**
    @name jake.TestTask#testFiles
    @public
    @type {jake.FileList}
    @description The list of files containing tests to load
   */
  this.testFiles = new jake.FileList();

  /**
    @name jake.TestTask#showDescription
    @public
    @type {Boolean}
    @description Show the created task when doing Jake -T
   */
  this.showDescription = true;

  /*
    @name jake.TestTask#totalTests
    @public
    @type {Number}
    @description The total number of tests to run
  */
  this.totalTests = 0;

  /*
    @name jake.TestTask#executedTests
    @public
    @type {Number}
    @description The number of tests successfully run
  */
  this.executedTests = 0;

  if (typeof definition == 'function') {
    definition.call(this);
  }

  if (this.showDescription) {
    desc('Run the tests for ' + name);
  }

  task(this.testName, prereqs, {async: true}, function () {
    var t = jake.Task[self.testName + ':run'];
    t.on('complete', function () {
      complete();
    });
    // Pass args to the namespaced test
    t.invoke.apply(t, arguments);
  });

  namespace(self.testName, function () {

    task('run', {async: true}, function (pat) {
      var p = pat || '.*'
        , re
        , testFiles;

      // Don't nest; make a top-level namespace. Don't want
      // re-calling from inside to nest infinitely
     jake.currentNamespace = jake.defaultNamespace;

      re = new RegExp(pat);
      // Get test files that match the passed-in pattern
      testFiles = self.testFiles.toArray()
          .filter(function (f) {
        return (re).test(f);
      }) // Don't load the same file multiple times -- should this be in FileList?
          .reduce(function(p, c) {
        if (p.indexOf(c) < 0) {
          p.push(c);
        }
        return p;
      }, []);

      // Create a namespace for all the testing tasks to live in
      namespace(self.testName + 'Exec', function () {
        // Each test will be a prereq for the dummy top-level task
        var prereqs = []
        // Continuation to pass to the async tests, wrapping 'continune'
          , next = function () {
              complete();
            }
        // Create the task for this test-function
          , createTask = function (name, action) {
              // If the test-function is defined with a continuation
              // param, flag the task as async
              var t
                , isAsync = !!action.length;

              // Define the actual namespaced task with the name, the
              // wrapped action, and the correc async-flag
              t = task(name, createAction(name, action), {
                async: isAsync
              });
              t.once('complete', function () {
                self.executedTests++;
              });
            }
        // Used as the action for the defined task for each test.
          , createAction = function (n, a) {
              // A wrapped function that passes in the 'next' function
              // for any tasks that run asynchronously
              return function () {
                var cb
                  , msg;
                if (a.length) {
                  cb = next;
                }
                if (!(n == 'before' || n == 'after' ||
                    /_beforeEach$/.test(n) || /_afterEach$/.test(n))) {
                  if (n.toLowerCase().indexOf('test') === 0) {
                    msg = n;
                  }
                  else {
                    msg = 'test ' + n;
                  }
                  jake.logger.log(n);
                }
                // 'this' will be the task when action is run
                return a.call(this, cb);
              };
            } ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.WatchTask"></a>[function <span class="apidocSignatureSpan">jake.</span>WatchTask ()](#apidoc.element.jake.WatchTask)
- description and source-code
```javascript
WatchTask = function () {
  var self = this
    , args = Array.prototype.slice.call(arguments)
    , arg
    , definition
    , taskNames
    , name
    , last = (new Date()).getTime() - THROTTLE;

  args = args.filter(function (a) {
    return !!a;
  });

  while ((arg = args.shift())) {
    if (typeof arg == 'string') {
      name = arg;
    }
    else if (typeof arg == 'object' && Array.isArray(arg)) {
      taskNames = arg;
    }
    else if (typeof arg == 'function') {
      definition = arg;
    }
  }

  if (!(taskNames && taskNames.length)) {
    throw new Error('Watch task needs some tasks to run');
  }

  name = name || 'watch';
  definition = definition || function () {};

  if (jake.Task[name]) {
    throw new Error('WatchTask named "' + name + '" already exists. ' +
      'Please use a different name.');
  }

  this.watchTasks = Array.isArray(taskNames) ? taskNames : [taskNames];
  this.watchFiles = new FileList();
  this.rootTask = task('watchTasks', this.watchTasks);
  this.throttle = THROTTLE;

  this.watchFiles.include(WatchTask.DEFAULT_INCLUDE_FILES);
  this.watchFiles.exclude(WatchTask.DEFAULT_EXCLUDE_FILES);

  if (typeof definition == 'function') {
    definition.call(this);
  }

  desc('Runs these tasks: ' + this.watchTasks.join(', '));
  task(name, function () {
    console.log('WatchTask started for: ' + self.watchTasks.join(', '));
    jake.watch('.', {includePattern: /.+/}, function (filePath) {
      var fileMatch = self.watchFiles.toArray().some(function (item) {
        return item == filePath;
      });
      if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
        last = (new Date()).getTime();
        self.rootTask.reenable(true);
        self.rootTask.invoke();
      }
    });
  });
}
```
- example usage
```shell
...

// Backward-compat
this.npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

this.watchTask = function (name, taskNames, definition) {
  return new jake.WatchTask(name, taskNames, definition);
};

this.testTask = function () {
  var ctor = function () {}
    , t;
  ctor.prototype = jake.TestTask.prototype;
  t = new ctor();
...
```

#### <a name="apidoc.element.jake.absolutize"></a>[function <span class="apidocSignatureSpan">jake.</span>absolutize (p)](#apidoc.element.jake.absolutize)
- description and source-code
```javascript
absolutize = function (p) {
  if (this.isAbsolute(p)) {
    return p;
  }
  else {
    return path.join(process.cwd(), p);
  }
}
```
- example usage
```shell
...
  isLiveScript = existsSync(jakefile + '.ls');
  if (isCoffee) {
    CoffeeScript = _requireCoffee();
  }
  if (isLiveScript) {
      LiveScript = _requireLiveScript();
  }
  require(utils.file.absolutize(jakefile));
  return true;
};

this.loadDirectory = function (d) {
  var dirname = d || 'jakelib'
    , dirlist;
  dirname = utils.file.absolutize(dirname);
...
```

#### <a name="apidoc.element.jake.async.AsyncChain"></a>[function <span class="apidocSignatureSpan">jake.</span>async.AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain)
- description and source-code
```javascript
async.AsyncChain = function (chain) {
  this.init(chain);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncGroup"></a>[function <span class="apidocSignatureSpan">jake.</span>async.AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup)
- description and source-code
```javascript
async.AsyncGroup = function (group) {
  var item;
  var callback;
  var args;

  this.group = [];
  this.outstandingCount = 0;

  for (var i = 0; i < group.length; i++) {
    item = group[i];
    this.group.push(new async.AsyncCall(
        item.func, item.args, item.callback, item.context));
    this.outstandingCount++;
  }

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.Initializer"></a>[function <span class="apidocSignatureSpan">jake.</span>async.Initializer (steps, callback)](#apidoc.element.jake.async.Initializer)
- description and source-code
```javascript
async.Initializer = function (steps, callback) {
  var self = this;
  this.steps = {};
  this.callback = callback;
  // Create an object-literal of the steps to tick off
  steps.forEach(function (step) {
    self.steps[step] = false;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.SimpleAsyncChain"></a>[function <span class="apidocSignatureSpan">jake.</span>async.SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain)
- description and source-code
```javascript
async.SimpleAsyncChain = function (funcs, context) {
  var chain = [];
  for (var i = 0, ii = funcs.length; i < ii; i++) {
    chain.push(_createSimpleAsyncCall(funcs[i], context));
  }
  this.init(chain);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.attemptRule"></a>[function <span class="apidocSignatureSpan">jake.</span>attemptRule (name, ns, level)](#apidoc.element.jake.attemptRule)
- description and source-code
```javascript
attemptRule = function (name, ns, level) {
  var prereqRule
    , prereq;
  if (level > MAX_RULE_RECURSION_LEVEL) {
    return null;
  }
  // Check Rule
  prereqRule = ns.matchRule(name);
  if (prereqRule) {
    prereq = prereqRule.createTask(name, level);
  }
  return prereq || null;
}
```
- example usage
```shell
...
// 1. an existing task
// 2. an existing file on disk
// 3. a valid rule (i.e., not at too deep a level)
valid = prereqs.some(function (p) {
  var ns = self.ns;
  return ns.resolveTask(p) ||
    fs.existsSync(Task.getBaseTaskName(p)) ||
    jake.attemptRule(p, ns, level + 1);
});

// If any of the prereqs aren't valid, the rule isn't valid
if (!valid) {
  return null;
}
// Otherwise, hunky-dory, finish creating the task for the rule
...
```

#### <a name="apidoc.element.jake.basedir"></a>[function <span class="apidocSignatureSpan">jake.</span>basedir (pathParam)](#apidoc.element.jake.basedir)
- description and source-code
```javascript
basedir = function (pathParam) {
  var basedir = ''
    , parts
    , part
    , pos = 0
    , p = pathParam || '';

  // If the path has a leading asterisk, basedir is the current dir
  if (p.indexOf('*') == 0 || p.indexOf('**') == 0) {
    return '.';
  }

  // always consider .. at the end as a folder and not a filename
  if (/(?:^|\/|\\)\.\.$/.test(p.slice(-3))) {
    p += '/';
  }

  parts = p.split(/\\|\//);
  for (var i = 0, l = parts.length - 1; i < l; i++) {
    part = parts[i];
    if (part.indexOf('*') > -1 || part.indexOf('**') > -1) {
      break;
    }
    pos += part.length + 1;
    basedir += part + p[pos - 1];
  }
  if (!basedir) {
    basedir = '.';
  }
  // Strip trailing slashes
  if (!(basedir == '\\' || basedir == '/')) {
    basedir = basedir.replace(/\\$|\/$/, '');
  }
  return basedir;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.bind"></a>[function <span class="apidocSignatureSpan">jake.</span>bind ()](#apidoc.element.jake.bind)
- description and source-code
```javascript
bind = function () {
  var args = Array.prototype.slice.call(arguments)
    , ctxt = args.shift()
    , fn = args.shift();

  if (typeof fn === 'function') {
    if (typeof Function.bind === 'function') {
      return fn.bind.apply(ctxt, args);
    }
    else {
      return fn.apply(ctxt, args);
    }
  }
  // in IE, native methods are not functions so they cannot be bound,
  // and don't need to be
  else {
    return fn;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.complete"></a>[function <span class="apidocSignatureSpan">jake.</span>complete (task, val)](#apidoc.element.jake.complete)
- description and source-code
```javascript
complete = function (task, val) {
  //this should detect if the first arg is a task, but I guess it should be more thorough
  if(task && task. _currentPrereqIndex >=0 ) {
    task.complete(val);
  } else {
    val = task;
    if(jake._invocationChain.length > 0) {
      jake._invocationChain[jake._invocationChain.length-1].complete(val);
    } else {
    }
  }
}
```
- example usage
```shell
...
@static
@function
@description Completes an asynchronous task, allowing Jake's
execution to proceed to the next task. Calling complete globally or without
arguments completes the last task on the invocationChain. If you use parallel
execution of prereqs this will probably complete a wrong task. You should call this
function with this task as the first argument, before the optional return value.
Alternatively you can call task.complete()
'
@example
task('generate', ['doc:clobber'], function () {
  exec('./generate_docs.sh', function (err, stdout, stderr) {
    if (err || stderr) {
      fail(err || stderr);
    }
...
```

#### <a name="apidoc.element.jake.cpR"></a>[function <span class="apidocSignatureSpan">jake.</span>cpR (fromPath, toPath, options)](#apidoc.element.jake.cpR)
- description and source-code
```javascript
cpR = function (fromPath, toPath, options) {
  var from = path.normalize(fromPath)
    , to = path.normalize(toPath)
    , toStat
    , doesNotExistErr
    , filename
    , opts = options || {};

  if (!opts.silent) {
    logger.log('cp -r ' + fromPath + ' ' + toPath);
  }

  if (from == to) {
    throw new Error('Cannot copy ' + from + ' to itself.');
  }

  // Handle rename-via-copy
  try {
    toStat = fs.statSync(to);
  }
  catch(e) {
    doesNotExistErr = e;

    // Get abs path so it's possible to check parent dir
    if (!this.isAbsolute(to)) {
      to = path.join(process.cwd() , to);
    }

    // Save the file/dir name
    filename = path.basename(to);
    // See if a parent dir exists, so there's a place to put the
    /// renamed file/dir (resets the destination for the copy)
    to = path.dirname(to);
    try {
      toStat = fs.statSync(to);
    }
    catch(e) {}
    if (toStat && toStat.isDirectory()) {
      // Set the rename opt to pass to the copy func, will be used
      // as the new file/dir name
      opts.rename = filename;
      //console.log('filename ' + filename);
    }
    else {
      throw doesNotExistErr;
    }
  }

  _copyFile(from, to, opts);
}
```
- example usage
```shell
...
    // Target is a directory, just create it
    if (stat.isDirectory()) {
      jake.mkdirP(file.to, {silent: true});
      _copyFile();
    }
    // Otherwise copy the file
    else {
      jake.cpR(file.from, file.to, {silent: true});
      _copyFile();
    }
  }
  else {
    complete();
  }
};
...
```

#### <a name="apidoc.element.jake.createExec"></a>[function <span class="apidocSignatureSpan">jake.</span>createExec (a, b, c)](#apidoc.element.jake.createExec)
- description and source-code
```javascript
createExec = function (a, b, c) {
  return new Exec(a, b, c);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.createPlaceholderFileTask"></a>[function <span class="apidocSignatureSpan">jake.</span>createPlaceholderFileTask (name, namespace)](#apidoc.element.jake.createPlaceholderFileTask)
- description and source-code
```javascript
createPlaceholderFileTask = function (name, namespace) {
  var nsPath = ''
    , filePath = name.split(':').pop() // Strip any namespace
    , parts
    , fileTaskName
    , task
    , stats;

  if (namespace) {
    if (typeof namespace == 'string') {
      nsPath = namespace;
    }
    else {
      nsPath = namespace.path;
    }
  }

  parts = nsPath.length ? nsPath.split(':') : [];
  parts.push(filePath);
  fileTaskName = parts.join(':');

  task = jake.Task[fileTaskName];

  // If there's not already an existing dummy FileTask for it,
  // create one
  if (!task) {
    // Create a dummy FileTask only if file actually exists
    if (fs.existsSync(filePath)) {
      stats = fs.statSync(filePath);
      task = new jake.FileTask(filePath);
      task.fullName = fileTaskName;
      task.modTime = stats.mtime;
      task.dummy = true;
      // Put this dummy Task in the global Tasks list so
      // modTime will be eval'd correctly
      jake.Task[fileTaskName] = task;
    }
  }

  return task || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.createTask"></a>[function <span class="apidocSignatureSpan">jake.</span>createTask ()](#apidoc.element.jake.createTask)
- description and source-code
```javascript
createTask = function () {
  var args = Array.prototype.slice.call(arguments)
    , arg
    , obj
    , task
    , type
    , name
    , action
    , opts = {}
    , prereqs = [];

    type = args.shift();

  // name, [deps], [action]
  // Name (string) + deps (array) format
  if (typeof args[0] == 'string') {
    name = args.shift();
    if (Array.isArray(args[0])) {
      prereqs = args.shift();
    }
  }
  // name:deps, [action]
  // Legacy object-literal syntax, e.g.: {'name': ['depA', 'depB']}
  else {
    obj = args.shift();
    for (var p in obj) {
      prereqs = prereqs.concat(obj[p]);
      name = p;
    }
  }

  // Optional opts/callback or callback/opts
  while ((arg = args.shift())) {
    if (typeof arg == 'function') {
      action = arg;
    }
    else {
      opts = arg;
    }
  }

  task = jake.currentNamespace.resolveTask(name);
  if (task && !action) {
    // Task already exists and no action, just update prereqs, and return it.
    task.prereqs = task.prereqs.concat(prereqs);
    return task;
  }

  switch (type) {
    case 'directory':
      action = function () {
        jake.mkdirP(name);
      };
      task = new DirectoryTask(name, prereqs, action, opts);
      break;
    case 'file':
      task = new FileTask(name, prereqs, action, opts);
      break;
    default:
      task = new Task(name, prereqs, action, opts);
  }

  if (jake.currentTaskDescription) {
    task.description = jake.currentTaskDescription;
    jake.currentTaskDescription = null;
  }
  jake.currentNamespace.tasks[name] = task;
  task.namespace = jake.currentNamespace;

  // FIXME: Should only need to add a new entry for the current
  // task-definition, not reparse the entire structure
  jake.parseAllTasks();

  return task;
}
```
- example usage
```shell
...
    // Insert the file task into Jake
    //
    // Since createTask function stores the task as a child task
    // of currentNamespace. Here we temporariliy switch the namespace.
    // FIXME: Should allow optional ns passed in instead of this hack
    tNs = jake.currentNamespace;
    jake.currentNamespace = ns;
    createdTask = jake.createTask('file', name, prereqs, action, opts);
    createdTask.source = src.split(':').pop();
    jake.currentNamespace = tNs;

    return createdTask;
  }

};
...
```

#### <a name="apidoc.element.jake.desc"></a>[function <span class="apidocSignatureSpan">jake.</span>desc (description)](#apidoc.element.jake.desc)
- description and source-code
```javascript
desc = function (description) {
  jake.currentTaskDescription = description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.directory"></a>[function <span class="apidocSignatureSpan">jake.</span>directory (name)](#apidoc.element.jake.directory)
- description and source-code
```javascript
directory = function (name) {
  var args = Array.prototype.slice.call(arguments)
    , createdTask;
  args.unshift('directory');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.enhance"></a>[function <span class="apidocSignatureSpan">jake.</span>enhance ()](#apidoc.element.jake.enhance)
- description and source-code
```javascript
enhance = function () {
  var args = Array.prototype.slice.apply(arguments),
      merge = false,
      targ, sources;
  if (args.length > 2) {
    if (typeof args[args.length - 1] == 'boolean') {
      merge = args.pop();
    }
  }
  targ = args.shift();
  sources = args;
  for (var i = 0, ii = sources.length; i < ii; i++) {
    _mix(targ, sources[i], merge, true);
  }
  return targ;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.exec"></a>[function <span class="apidocSignatureSpan">jake.</span>exec (a, b, c)](#apidoc.element.jake.exec)
- description and source-code
```javascript
exec = function (a, b, c) {
  var parsed = parseArgs(arguments)
    , cmds = parsed.cmds
    , opts = parsed.opts
    , callback = parsed.callback;

  var ex = new Exec(cmds, opts, callback);

  ex.addListener('error', function (msg, code) {
    if (opts.breakOnError) {
      fail(msg, code);
    }
  });
  ex.run();

  return ex;
}
```
- example usage
```shell
...
  If you flag a task with this option, you must call the global
  'complete' method inside the task's action, for execution to proceed
  to the next task.
@example
desc('This is a rule, which does not support namespace or pattern.');
rule('.o', '.c', {async: true}, function () {
  var cmd = util.format('gcc -o %s %s', this.name, this.source);
  jake.exec([cmd], function () {
    complete();
  }, {printStdout: true});
});

desc('This rule has prerequisites.');
rule('.o', '.c', ['util.h'], {async: true}, function () {
  var cmd = util.format('gcc -o %s %s', this.name, this.source);
...
```

#### <a name="apidoc.element.jake.exists"></a>[function <span class="apidocSignatureSpan">jake.</span>exists (path, callback)](#apidoc.element.jake.exists)
- description and source-code
```javascript
exists = function (path, callback) {
  if (!nullCheck(path, cb)) return;
  var req = new FSReqWrap();
  req.oncomplete = cb;
  binding.stat(pathModule._makeLong(path), req);
  function cb(err, stats) {
    if (callback) callback(err ? false : true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.existsSync"></a>[function <span class="apidocSignatureSpan">jake.</span>existsSync (path)](#apidoc.element.jake.existsSync)
- description and source-code
```javascript
existsSync = function (path) {
  try {
    nullCheck(path);
    binding.stat(pathModule._makeLong(path), statValues);
    return true;
  } catch (e) {
    return false;
  }
}
```
- example usage
```shell
...
 If this argument is an Error object, it will simply be thrown. If
 a String, it will be used as the error-message. (If it is a multi-line
 String, the first line will be used as the Error message, and the
 remaining lines will be used as the error-stack.)

 @example
 task('createTests, function () {
   if (!fs.existsSync('./tests')) {
     fail('Test directory does not exist.');
   }
   else {
     // Do some testing stuff ...
   }
 });
*/
...
```

#### <a name="apidoc.element.jake.fail"></a>[function <span class="apidocSignatureSpan">jake.</span>fail (err, code)](#apidoc.element.jake.fail)
- description and source-code
```javascript
fail = function (err, code) {
  var msg
    , errObj;
  if (code) {
    jake.errorCode = code;
  }
  if (err) {
    if (typeof err == 'string') {
      // Use the initial or only line of the error as the error-message
      // If there was a multi-line error, use the rest as the stack
      msg = err.split('\n');
      errObj = new Error(msg.shift());
      if (msg.length) {
        errObj.stack = msg.join('\n');
      }
      throw errObj;
    }
    else if (err instanceof Error) {
      throw err;
    }
    else {
      throw new Error(err.toString());
    }
  }
  else {
    throw new Error();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.file"></a>[function <span class="apidocSignatureSpan">jake.</span>file (name, prereqs, action, opts)](#apidoc.element.jake.file)
- description and source-code
```javascript
file = function (name, prereqs, action, opts) {
  var args = Array.prototype.slice.call(arguments)
    , createdTask;
  args.unshift('file');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.init"></a>[function <span class="apidocSignatureSpan">jake.</span>init ()](#apidoc.element.jake.init)
- description and source-code
```javascript
init = function () {
  var self = this;
  process.addListener('uncaughtException', function (err) {
    self.program.handleErr(err);
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.isAbsolute"></a>[function <span class="apidocSignatureSpan">jake.</span>isAbsolute (p)](#apidoc.element.jake.isAbsolute)
- description and source-code
```javascript
isAbsolute = function (p) {
  var match = /^[A-Za-z]+:\\|^\//.exec(p);
  if (match && match.length) {
    return match[0];
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.isEmpty"></a>[function <span class="apidocSignatureSpan">jake.</span>isEmpty (val)](#apidoc.element.jake.isEmpty)
- description and source-code
```javascript
isEmpty = function (val) {
  // Empty string, null or undefined (these two are double-equal)
  if (val === '' || val == undefined) {
    return true;
  }
  // Invalid numerics
  if (typeof val == 'number' && isNaN(val)) {
    return true;
  }
  // Invalid Dates
  if (val instanceof Date && isNaN(val.getTime())) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log"></a>[function <span class="apidocSignatureSpan">jake.</span>log (obj)](#apidoc.element.jake.log)
- description and source-code
```javascript
log = function (obj) {
  _output(obj, 'info');
}
```
- example usage
```shell
...
  If you flag a task with this option, you must call the global
  'complete' method inside the task's action, for execution to proceed
  to the next task.

@example
desc('This is the default task.');
task('default', function (params) {
  console.log('This is the default task.');
});

desc('This task has prerequisites.');
task('hasPrereqs', ['foo', 'bar', 'baz'], function (params) {
  console.log('Ran some prereqs first.');
});
...
```

#### <a name="apidoc.element.jake.mixin"></a>[function <span class="apidocSignatureSpan">jake.</span>mixin ()](#apidoc.element.jake.mixin)
- description and source-code
```javascript
mixin = function () {
  var args = Array.prototype.slice.apply(arguments),
      merge = false,
      targ, sources;
  if (args.length > 2) {
    if (typeof args[args.length - 1] == 'boolean') {
      merge = args.pop();
    }
  }
  targ = args.shift();
  sources = args;
  for (var i = 0, ii = sources.length; i < ii; i++) {
    _mix(targ, sources[i], merge);
  }
  return targ;
}
```
- example usage
```shell
...
  this.setOpts(result.opts);
  this.setTaskNames(result.taskNames);
  this.setEnvVars(result.envVars);
};

this.setOpts = function (options) {
  var opts = options || {};
  utils.mixin(this.opts, opts);
};

this.setTaskNames = function (names) {
  if (names && !Array.isArray(names)) {
    throw new Error('Task names must be an array');
  }
  this.taskNames = (names && names.length) ? names : ['default'];
...
```

#### <a name="apidoc.element.jake.mkdirP"></a>[function <span class="apidocSignatureSpan">jake.</span>mkdirP (dir, mode)](#apidoc.element.jake.mkdirP)
- description and source-code
```javascript
mkdirP = function (dir, mode) {
  var dirPath = path.normalize(dir)
    , paths = dirPath.split(/\/|\\/)
    , currPath = ''
    , next;

  if (paths[0] == '' || /^[A-Za-z]+:/.test(paths[0])) {
    currPath = paths.shift() || '/';
    currPath = path.join(currPath, paths.shift());
    //console.log('basedir');
  }
  while ((next = paths.shift())) {
    if (next == '..') {
      currPath = path.join(currPath, next);
      continue;
    }
    currPath = path.join(currPath, next);
    try {
      //console.log('making ' + currPath);
      fs.mkdirSync(currPath, mode || parseInt(755, 8));
    }
    catch(e) {
      if (e.code != 'EEXIST') {
        throw e;
      }
    }
  }
}
```
- example usage
```shell
...
}

task('buildPackage', compressTaskArr, function () {});

directory(this.packageDir);

file(packageDirPath, this.packageFiles, function () {
  jake.mkdirP(packageDirPath);
  var fileList = [];
  self.packageFiles.forEach(function (name) {
    var f = path.join(self.packageDirPath(), name)
      , fDir = path.dirname(f)
      , stats;
    jake.mkdirP(fDir, {silent: true});
...
```

#### <a name="apidoc.element.jake.namespace"></a>[function <span class="apidocSignatureSpan">jake.</span>namespace (name, closure)](#apidoc.element.jake.namespace)
- description and source-code
```javascript
namespace = function (name, closure) {
  var curr = jake.currentNamespace
    , ns = curr.childNamespaces[name] || new jake.Namespace(name, curr);
  curr.childNamespaces[name] = ns;
  jake.currentNamespace = ns;
  closure();
  jake.currentNamespace = curr;
  jake.currentTaskDescription = null;
  return ns;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.npmPublishTask"></a>[function <span class="apidocSignatureSpan">jake.</span>npmPublishTask (name, prereqs, opts, definition)](#apidoc.element.jake.npmPublishTask)
- description and source-code
```javascript
npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.packageTask"></a>[function <span class="apidocSignatureSpan">jake.</span>packageTask (name, version, definition)](#apidoc.element.jake.packageTask)
- description and source-code
```javascript
packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.parseAllTasks"></a>[function <span class="apidocSignatureSpan">jake.</span>parseAllTasks ()](#apidoc.element.jake.parseAllTasks)
- description and source-code
```javascript
parseAllTasks = function () {
  var _parseNs = function (name, ns) {
    var nsTasks = ns.tasks
      , task
      , nsNamespaces = ns.childNamespaces
      , fullName;
    // Iterate through the tasks in each namespace
    for (var q in nsTasks) {
      task = nsTasks[q];
      // Prefix namespaced tasks
      fullName = name == 'default' ? q : name + ':' + q;
      // Save with 'taskname' or 'namespace:taskname' key
      task.fullName = fullName;
      jake.Task[fullName] = task;
    }
    for (var p in nsNamespaces) {
      fullName = (name == 'default') ? p : name + ':' + p;
      _parseNs(fullName, nsNamespaces[p]);
    }
  };

  _parseNs('default', jake.defaultNamespace);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.publishTask"></a>[function <span class="apidocSignatureSpan">jake.</span>publishTask (name, prereqs, opts, definition)](#apidoc.element.jake.publishTask)
- description and source-code
```javascript
publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.readdirR"></a>[function <span class="apidocSignatureSpan">jake.</span>readdirR (dir, opts)](#apidoc.element.jake.readdirR)
- description and source-code
```javascript
readdirR = function (dir, opts) {
  var options = opts || {}
    , format = options.format || 'array'
    , ret;
  ret = _readDir(dir);
  return format == 'string' ? ret.join('\n') : ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.request"></a>[function <span class="apidocSignatureSpan">jake.</span>request (opts, callback)](#apidoc.element.jake.request)
- description and source-code
```javascript
request = function (opts, callback) {
  var client
    , options = opts || {}
    , parsed = url.parse(options.url)
    , path
    , requester = parsed.protocol == 'http:' ? http : https
    , method = (options.method && options.method.toUpperCase()) || 'GET'
    , headers = core.mixin({}, options.headers || {})
    , data = options.data
    , contentLength
    , port
    , clientOpts;

  if (parsed.port) {
    port = parsed.port;
  }
  else {
    port = parsed.protocol == 'http:' ? '80' : '443';
  }

  path = parsed.pathname;

  if (method == 'POST' || method == 'PUT') {
    // Handle the payload and content-length
    if (data) {
      // JSON data
      if (options.dataType == 'json') {
        if (typeof data == 'object') {
          data = JSON.stringify(data);
        }
        headers['Content-Type'] = headers['Content-Type'] ||
            headers['content-type'] || 'application/json';
      }
      // Form data
      else {
        if (typeof data == 'object') {
          data = uri.paramify(data);
        }
        // FIXME: What is the prefix for form-urlencoded?
        headers['Content-Type'] = headers['Content-Type'] ||
            headers['content-type'] || 'form-urlencoded';
      }
      contentLength = Buffer.byteLength(data);
    }
    else {
      contentLength = 0
    }
    headers['Content-Length'] = contentLength;

    if (parsed.search) {
      path += parsed.search;
    }
  }
  else {
    if (data) {
      // Data is an object, parse into querystring
      if (typeof data == 'object') {
        data = uri.paramify(data);
      }
      // Create querystring or append to existing
      if (parsed.search) {
        path += parsed.search; // search includes question mark
        path += '&' + data;
      }
      else {
        path += '?' + data;
      }
    }
  }

  clientOpts = {
    host: parsed.hostname
  , port: port
  , method: method
  , agent: false
  , path: path
  , headers: headers
  };
  client = requester.request(clientOpts);

  client.addListener('response', function (resp) {
    var data = '';

    resp.addListener('data', function (chunk) {
      data += chunk.toString();
    });

    resp.addListener('end', function () {
      var stat = resp.statusCode
        , contentType
        , err;
      // Successful response
      if ((stat > 199 && stat < 300) || stat == 304) {
        if (data) {
          contentType = resp.headers['Content-Type'];
          if (contentType == 'application/json' || contentType == 'text/json' ||
            uri.getFileExtension(parsed.pathname) == 'json') {
            try {
                data = JSON.parse(data);
            }
            catch (e) {
              return callback(e, null);
            }
          }
          callback(null, data);
        }
        else {
          callback(null, null);
        }
      }
      // Something failed
      else {
        err = new Error(data);
        err.statusCode = resp.statusCode;
        callback(err, null);
      }

    });
  });

  client.addListener('error', function (e) {
    callback(e, null);
  });

  if ((method == 'POST' || method == 'PUT') && data) {
    client.write(data);
  }

  client.end();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.requireLocal"></a>[function <span class="apidocSignatureSpan">jake.</span>requireLocal (module, message)](#apidoc.element.jake.requireLocal)
- description and source-code
```javascript
requireLocal = function (module, message) {
  var dep;
  // Try to require in the application directory
  try {
    dep = require(path.join(process.cwd(), 'node_modules', module));
  }
  catch(err) {
    if (message) {
      throw new Error(message);
    }
    throw new Error('Module "' + module + '" could not be found as a ' +
        'local module. Please install it by doing "npm install ' +
        module + '"');
  }
  return dep;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.rmRf"></a>[function <span class="apidocSignatureSpan">jake.</span>rmRf (p, options)](#apidoc.element.jake.rmRf)
- description and source-code
```javascript
rmRf = function (p, options) {
  var stat
    , opts = options || {};
  if (!opts.silent) {
    logger.log('rm -rf ' + p);
  }
  try {
    stat = fs.lstatSync(p);
    if (stat.isDirectory()) {
      _rmDir(p);
    }
    else {
      fs.unlinkSync(p);
    }
  }
  catch (e) {}
}
```
- example usage
```shell
...

desc('Build the package for distribution');
task('package', self.prereqs.concat(['clobberPackage', 'buildPackage']));
// Backward-compat alias
task('repackage', ['package']);

task('clobberPackage', function () {
  jake.rmRf(self.packageDir, {silent: true});
});

desc('Remove the package');
task('clobber', ['clobberPackage']);

var doCommand = function (p) {
  var filename = path.resolve(self.packageDir + '/' + self.packageName() +
...
```

#### <a name="apidoc.element.jake.rule"></a>[function <span class="apidocSignatureSpan">jake.</span>rule ()](#apidoc.element.jake.rule)
- description and source-code
```javascript
rule = function () {
  var args = Array.prototype.slice.call(arguments)
    , arg
    , pattern = args.shift()
    , source = args.shift()
    , prereqs = []
    , action = function () {}
    , opts = {}
    , key = pattern.toString(); // May be a RegExp

  while ((arg = args.shift())) {
    if (typeof arg == 'function') {
      action = arg;
    }
    else if (Array.isArray(arg)) {
      prereqs = arg;
    }
    else {
      opts = arg;
    }
  }

  jake.currentNamespace.rules[key] = new jake.Rule({
    pattern: pattern
  , source: source
  , prereqs: prereqs
  , action: action
  , opts: opts
  , desc: jake.currentTaskDescription
  , ns: jake.currentNamespace
  });
  jake.currentTaskDescription = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.run"></a>[function <span class="apidocSignatureSpan">jake.</span>run ()](#apidoc.element.jake.run)
- description and source-code
```javascript
run = function () {
  var args = Array.prototype.slice.call(arguments)
    , program = this.program
    , loader = this.loader
    , preempt
    , opts;

  program.parseArgs(args);
  program.init();

  preempt = program.firstPreemptiveOption();
  if (preempt) {
    preempt();
  }
  else {
    opts = program.opts;
    // Load Jakefile and jakelibdir files
    var jakefileLoaded = loader.loadFile(opts.jakefile);
    var jakelibdirLoaded = loader.loadDirectory(opts.jakelibdir);

    if(!jakefileLoaded && !jakelibdirLoaded) {
      fail('No Jakefile. Specify a valid path with -f/--jakefile, ' +
          'or place one in the current directory.');
    }

    program.run();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.searchParentPath"></a>[function <span class="apidocSignatureSpan">jake.</span>searchParentPath (location, beginPath, callback)](#apidoc.element.jake.searchParentPath)
- description and source-code
```javascript
searchParentPath = function (location, beginPath, callback) {
  if (typeof beginPath === 'function' && !callback) {
    callback = beginPath;
    beginPath = process.cwd();
  }
  var cwd = beginPath || process.cwd();

  if (!location) {
    // Return if no path is given
    return;
  }
  var relPath = ''
    , i = 5 // Only search up to 5 directories
    , pathLoc
    , pathExists;

  while (--i >= 0) {
    pathLoc = path.join(cwd, relPath, location);
    pathExists = this.existsSync(pathLoc);

    if (pathExists) {
      callback && callback(undefined, pathLoc);
      break;
    } else {
      // Dir could not be found
      if (i === 0) {
        callback && callback(new Error("Path \"" + pathLoc + "\" not found"), undefined);
        break;
      }

      // Add a relative parent directory
      relPath += '../';
      // Switch to relative parent directory
      process.chdir(path.join(cwd, relPath));
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.showAllTaskDescriptions"></a>[function <span class="apidocSignatureSpan">jake.</span>showAllTaskDescriptions (f)](#apidoc.element.jake.showAllTaskDescriptions)
- description and source-code
```javascript
showAllTaskDescriptions = function (f) {
  var p
    , maxTaskNameLength = 0
    , task
    , str = ''
    , padding
    , name
    , descr
    , filter = typeof f == 'string' ? f : null;

  for (p in jake.Task) {
    task = jake.Task[p];
    // Record the length of the longest task name -- used for
    // pretty alignment of the task descriptions
    maxTaskNameLength = p.length > maxTaskNameLength ?
      p.length : maxTaskNameLength;
  }
  // Print out each entry with descriptions neatly aligned
  for (p in jake.Task) {
    if (filter && p.indexOf(filter) == -1) {
      continue;
    }
    task = jake.Task[p];

    //name = '\033[32m' + p + '\033[39m ';
    name = chalk.green(p);

    // Create padding-string with calculated length
    padding = (new Array(maxTaskNameLength - p.length + 2)).join(' ');

    descr = task.description;
    if (descr) {
      descr = chalk.gray(descr);
      console.log('jake ' + name + padding + descr);
    }
  }
}
```
- example usage
```shell
...
var rootTask
  , taskNames
  , dirname
  , opts = this.opts;

// Run with 'jake -T', just show descriptions
if (opts.tasks) {
  return jake.showAllTaskDescriptions(opts.tasks);
}

taskNames = this.taskNames;
if (!(Array.isArray(taskNames) && taskNames.length)) {
  throw new Error('Please pass jake.runTasks an array of task-names');
}
...
```

#### <a name="apidoc.element.jake.task"></a>[function <span class="apidocSignatureSpan">jake.</span>task (name, prereqs, action, opts)](#apidoc.element.jake.task)
- description and source-code
```javascript
task = function (name, prereqs, action, opts) {
  var args = Array.prototype.slice.call(arguments)
    , type
    , createdTask;
  args.unshift('task');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.testTask"></a>[function <span class="apidocSignatureSpan">jake.</span>testTask ()](#apidoc.element.jake.testTask)
- description and source-code
```javascript
testTask = function () {
  var ctor = function () {}
    , t;
  ctor.prototype = jake.TestTask.prototype;
  t = new ctor();
  jake.TestTask.apply(t, arguments);
  return t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.watch"></a>[function <span class="apidocSignatureSpan">jake.</span>watch ()](#apidoc.element.jake.watch)
- description and source-code
```javascript
watch = function () {
  _watch.apply(this, arguments);
}
```
- example usage
```shell
...
if (typeof definition == 'function') {
  definition.call(this);
}

desc('Runs these tasks: ' + this.watchTasks.join(', '));
task(name, function () {
  console.log('WatchTask started for: ' + self.watchTasks.join(', '));
  jake.watch('.', {includePattern: /.+/}, function (filePath) {
    var fileMatch = self.watchFiles.toArray().some(function (item) {
      return item == filePath;
    });
    if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
      last = (new Date()).getTime();
      self.rootTask.reenable(true);
      self.rootTask.invoke();
...
```

#### <a name="apidoc.element.jake.watchTask"></a>[function <span class="apidocSignatureSpan">jake.</span>watchTask (name, taskNames, definition)](#apidoc.element.jake.watchTask)
- description and source-code
```javascript
watchTask = function (name, taskNames, definition) {
  return new jake.WatchTask(name, taskNames, definition);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.DirectoryTask"></a>[module jake.DirectoryTask](#apidoc.module.jake.DirectoryTask)

#### <a name="apidoc.element.jake.DirectoryTask.DirectoryTask"></a>[function <span class="apidocSignatureSpan">jake.</span>DirectoryTask (name)](#apidoc.element.jake.DirectoryTask.DirectoryTask)
- description and source-code
```javascript
DirectoryTask = function (name) {
  this.modTime = null;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.DirectoryTask.prototype"></a>[module jake.DirectoryTask.prototype](#apidoc.module.jake.DirectoryTask.prototype)

#### <a name="apidoc.element.jake.DirectoryTask.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jake.DirectoryTask.prototype.</span>constructor (name)](#apidoc.element.jake.DirectoryTask.prototype.constructor)
- description and source-code
```javascript
constructor = function (name) {
  this.modTime = null;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.EventBuffer"></a>[module jake.EventBuffer](#apidoc.module.jake.EventBuffer)

#### <a name="apidoc.element.jake.EventBuffer.EventBuffer"></a>[function <span class="apidocSignatureSpan">jake.</span>EventBuffer (src, events)](#apidoc.element.jake.EventBuffer.EventBuffer)
- description and source-code
```javascript
EventBuffer = function (src, events) {
  // By default, we service the default stream events
  var self = this
    , streamEvents = ['data', 'end', 'error', 'close', 'fd', 'drain', 'pipe'];
  this.events = events || streamEvents;
  this.emitter = src;
  this.eventBuffer = [];
  this.outlet = null;
  this.events.forEach(function (name) {
    self.emitter.addListener(name, function () {
      self.proxyEmit(name, arguments);
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.EventBuffer.prototype"></a>[module jake.EventBuffer.prototype](#apidoc.module.jake.EventBuffer.prototype)

#### <a name="apidoc.element.jake.EventBuffer.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>constructor (src, events)](#apidoc.element.jake.EventBuffer.prototype.constructor)
- description and source-code
```javascript
constructor = function (src, events) {
  // By default, we service the default stream events
  var self = this
    , streamEvents = ['data', 'end', 'error', 'close', 'fd', 'drain', 'pipe'];
  this.events = events || streamEvents;
  this.emitter = src;
  this.eventBuffer = [];
  this.outlet = null;
  this.events.forEach(function (name) {
    self.emitter.addListener(name, function () {
      self.proxyEmit(name, arguments);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.EventBuffer.prototype.emit"></a>[function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>emit (name, args)](#apidoc.element.jake.EventBuffer.prototype.emit)
- description and source-code
```javascript
emit = function (name, args) {
  // Prepend name to args
  var outlet = this.outlet;
  Array.prototype.splice.call(args, 0, 0, name);
  outlet.emit.apply(outlet, args);
}
```
- example usage
```shell
...
  this.envVars = null;
};

Program.prototype = new (function () {

  this.handleErr = function (err) {
if(jake.listeners('error').length !== 0) {
  jake.emit('error', err);
  return;
}

var msg;

if (jake.listeners('error').length) {
  jake.emit('error', err);
...
```

#### <a name="apidoc.element.jake.EventBuffer.prototype.proxyEmit"></a>[function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>proxyEmit (name, args)](#apidoc.element.jake.EventBuffer.prototype.proxyEmit)
- description and source-code
```javascript
proxyEmit = function (name, args) {
  if (this.outlet) {
    this.emit(name, args);
  }
  else {
    this.eventBuffer.push({name: name, args: args});
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.EventBuffer.prototype.sync"></a>[function <span class="apidocSignatureSpan">jake.EventBuffer.prototype.</span>sync (outlet)](#apidoc.element.jake.EventBuffer.prototype.sync)
- description and source-code
```javascript
sync = function (outlet) {
  var buffer = this.eventBuffer
    , bufferItem;
  this.outlet = outlet;
  while ((bufferItem = buffer.shift())) {
    this.emit(bufferItem.name, bufferItem.args);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.Exec"></a>[module jake.Exec](#apidoc.module.jake.Exec)

#### <a name="apidoc.element.jake.Exec.Exec"></a>[function <span class="apidocSignatureSpan">jake.</span>Exec ()](#apidoc.element.jake.Exec.Exec)
- description and source-code
```javascript
Exec = function () {
  var parsed = parseArgs(arguments)
    , cmds = parsed.cmds
    , opts = parsed.opts
    , callback = parsed.callback;

  this._cmds = cmds;
  this._callback = callback;
  this._config = opts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Exec.super_"></a>[function <span class="apidocSignatureSpan">jake.Exec.</span>super_ ()](#apidoc.element.jake.Exec.super_)
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



# <a name="apidoc.module.jake.Exec.prototype"></a>[module jake.Exec.prototype](#apidoc.module.jake.Exec.prototype)

#### <a name="apidoc.element.jake.Exec.prototype.append"></a>[function <span class="apidocSignatureSpan">jake.Exec.prototype.</span>append (cmd)](#apidoc.element.jake.Exec.prototype.append)
- description and source-code
```javascript
append = function (cmd) {
  this._cmds.push(cmd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Exec.prototype.run"></a>[function <span class="apidocSignatureSpan">jake.Exec.prototype.</span>run ()](#apidoc.element.jake.Exec.prototype.run)
- description and source-code
```javascript
run = function () {
  _run.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.FileList"></a>[module jake.FileList](#apidoc.module.jake.FileList)

#### <a name="apidoc.element.jake.FileList.FileList"></a>[function <span class="apidocSignatureSpan">jake.</span>FileList ()](#apidoc.element.jake.FileList.FileList)
- description and source-code
```javascript
FileList = function () {
  var self = this
    , wrap;

  // List of glob-patterns or specific filenames
  this.pendingAdd = [];
  // Switched to false after lazy-eval of files
  this.pending = true;
  // Used to calculate exclusions from the list of files
  this.excludes = {
    pats: DEFAULT_IGNORE_PATTERNS.slice()
  , funcs: DEFAULT_IGNORE_FUNCS.slice()
  , regex: null
  };
  this.items = [];

  // Wrap the array methods with the delegates
  wrap = function (prop) {
    var arr;
    self[prop] = function () {
      if (self.pending) {
        self.resolve();
      }
      if (typeof self.items[prop] == 'function') {
        // Special method that return a copy
        if (SPECIAL_RETURN[prop]) {
          arr = self.items[prop].apply(self.items, arguments);
          return FileList.clone(self, arr);
        }
        else {
          return self.items[prop].apply(self.items, arguments);
        }
      }
      else {
        return self.items[prop];
      }
    };
  };
  for (var i = 0, ii = ARRAY_METHODS.length; i < ii; i++) {
    wrap(ARRAY_METHODS[i]);
  }

  // Include whatever files got passed to the constructor
  this.include.apply(this, arguments);

  // Fix constructor linkage
  this.constructor = FileList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileList.clone"></a>[function <span class="apidocSignatureSpan">jake.FileList.</span>clone (list, items)](#apidoc.element.jake.FileList.clone)
- description and source-code
```javascript
clone = function (list, items) {
  var clone = new FileList();
  if (items) {
    clone.items = items;
  }
  clone.pendingAdd = list.pendingAdd;
  clone.pending = list.pending;
  for (var p in list.excludes) {
    clone.excludes[p] = list.excludes[p];
  }
  return clone;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.FileList.prototype"></a>[module jake.FileList.prototype](#apidoc.module.jake.FileList.prototype)

#### <a name="apidoc.element.jake.FileList.prototype.clearExclusions"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>clearExclusions ()](#apidoc.element.jake.FileList.prototype.clearExclusions)
- description and source-code
```javascript
clearExclusions = function () {
  this.excludes = {
    pats: []
  , funcs: []
  , regex: null
  };
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileList.prototype.clearInclusions"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>clearInclusions ()](#apidoc.element.jake.FileList.prototype.clearInclusions)
- description and source-code
```javascript
clearInclusions = function () {
  this.pendingAdd = [];
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileList.prototype.exclude"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>exclude ()](#apidoc.element.jake.FileList.prototype.exclude)
- description and source-code
```javascript
exclude = function () {
  var args = Array.isArray(arguments[0]) ? arguments[0] : arguments
    , arg;
  for (var i = 0, ii = args.length; i < ii; i++) {
    arg = args[i];
    if (typeof arg == 'function' && !(arg instanceof RegExp)) {
      this.excludes.funcs.push(arg);
    }
    else {
      this.excludes.pats.push(arg);
    }
  }
  if (!this.pending) {
    _resolveExclude.call(this);
  }
  return this;
}
```
- example usage
```shell
...
  , 'app/*'
  , 'bin/*'
  , 'config/*'
  , 'lib/*'
  , 'node_modules/*'
  ];
  this.packageFiles.include(files);
  this.packageFiles.exclude('node_modules/foobar');
  this.needTarGz = true;
});

 */
var PackageTask = function () {
var args = Array.prototype.slice.call(arguments)
  , name = args.shift()
...
```

#### <a name="apidoc.element.jake.FileList.prototype.include"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>include (items)](#apidoc.element.jake.FileList.prototype.include)
- description and source-code
```javascript
include = function (items) {
  if (items) {
    this.pendingAdd = this.pendingAdd.concat(items).filter(function (item) {
      return !!item;
    });
  }
  return this;
}
```
- example usage
```shell
...
  , 'package.json'
  , 'app/*'
  , 'bin/*'
  , 'config/*'
  , 'lib/*'
  , 'node_modules/*'
  ];
  this.packageFiles.include(files);
  this.packageFiles.exclude('node_modules/foobar');
  this.needTarGz = true;
});

 */
var PackageTask = function () {
var args = Array.prototype.slice.call(arguments)
...
```

#### <a name="apidoc.element.jake.FileList.prototype.resolve"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>resolve ()](#apidoc.element.jake.FileList.prototype.resolve)
- description and source-code
```javascript
resolve = function () {
  var name
    , uniqueFunc = function (p, c) {
        if (p.indexOf(c) < 0) {
          p.push(c);
        }
        return p;
      };
  if (this.pending) {
    this.pending = false;
    while ((name = this.pendingAdd.shift())) {
      _resolveAdd.call(this, name);
    }
    // Reduce to a unique list
    this.items = this.items.reduce(uniqueFunc, []);
    // Remove exclusions
    _resolveExclude.call(this);
  }
  return this;
}
```
- example usage
```shell
...
  jake.rmRf(self.packageDir, {silent: true});
});

desc('Remove the package');
task('clobber', ['clobberPackage']);

var doCommand = function (p) {
  var filename = path.resolve(self.packageDir + '/' + self.packageName() +
                              _compressOpts[p].ext);
  if (process.platform == 'win32') {
      // Windows full path may have drive letter, which is going to cause
      // namespace problems, so strip it.
      if (filename.length > 2 && filename[1] == ':') {
        filename = filename.substr(2);
      }
...
```

#### <a name="apidoc.element.jake.FileList.prototype.shouldExclude"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>shouldExclude (name)](#apidoc.element.jake.FileList.prototype.shouldExclude)
- description and source-code
```javascript
shouldExclude = function (name) {
  if (!this.excludes.regex) {
    _calculateExcludeRe.call(this);
  }
  var excl = this.excludes;
  return excl.regex.test(name) || excl.funcs.some(function (f) {
    return !!f(name);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileList.prototype.toArray"></a>[function <span class="apidocSignatureSpan">jake.FileList.prototype.</span>toArray ()](#apidoc.element.jake.FileList.prototype.toArray)
- description and source-code
```javascript
toArray = function () {
  // Call slice to ensure lazy-resolution before slicing items
  var ret = this.slice().items.slice();
  return ret;
}
```
- example usage
```shell
...
  definition.call(this);
}

desc('Runs these tasks: ' + this.watchTasks.join(', '));
task(name, function () {
  console.log('WatchTask started for: ' + self.watchTasks.join(', '));
  jake.watch('.', {includePattern: /.+/}, function (filePath) {
    var fileMatch = self.watchFiles.toArray().some(function (item) {
      return item == filePath;
    });
    if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
      last = (new Date()).getTime();
      self.rootTask.reenable(true);
      self.rootTask.invoke();
    }
...
```



# <a name="apidoc.module.jake.FileTask"></a>[module jake.FileTask](#apidoc.module.jake.FileTask)

#### <a name="apidoc.element.jake.FileTask.FileTask"></a>[function <span class="apidocSignatureSpan">jake.</span>FileTask (name, prereqs, action, opts)](#apidoc.element.jake.FileTask.FileTask)
- description and source-code
```javascript
FileTask = function (name, prereqs, action, opts) {
  this.modTime = null;
  this.dummy = false;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.FileTask.prototype"></a>[module jake.FileTask.prototype](#apidoc.module.jake.FileTask.prototype)

#### <a name="apidoc.element.jake.FileTask.prototype.complete"></a>[function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>complete ()](#apidoc.element.jake.FileTask.prototype.complete)
- description and source-code
```javascript
complete = function () {
  jake._invocationChain.splice(jake._invocationChain.indexOf(this),1);
  if (!this.dummy) {
    this.updateModTime();
  }
  this._currentPrereqIndex = 0;
  this.taskStatus = Task.runStatuses.DONE;
  this.emit('complete');
}
```
- example usage
```shell
...
@static
@function
@description Completes an asynchronous task, allowing Jake's
execution to proceed to the next task. Calling complete globally or without
arguments completes the last task on the invocationChain. If you use parallel
execution of prereqs this will probably complete a wrong task. You should call this
function with this task as the first argument, before the optional return value.
Alternatively you can call task.complete()
'
@example
task('generate', ['doc:clobber'], function () {
  exec('./generate_docs.sh', function (err, stdout, stderr) {
    if (err || stderr) {
      fail(err || stderr);
    }
...
```

#### <a name="apidoc.element.jake.FileTask.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>constructor (name, prereqs, action, opts)](#apidoc.element.jake.FileTask.prototype.constructor)
- description and source-code
```javascript
constructor = function (name, prereqs, action, opts) {
  this.modTime = null;
  this.dummy = false;
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileTask.prototype.isNeeded"></a>[function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>isNeeded ()](#apidoc.element.jake.FileTask.prototype.isNeeded)
- description and source-code
```javascript
isNeeded = function () {
  var runAction = false
    , prereqs = this.prereqs
    , prereqName
    , prereqTask;

  // No repeatsies
  if (this.taskStatus === Task.runStatuses.DONE) {
    return false;
  }
  // The always-make override
  else if (jake.program.opts['always-make']) {
    // Run if there actually is an action
    if (typeof this.action == 'function') {
      return true;
    }
    else {
      return false;
    }
  }
  // Default case
  else {
    // We need either an existing file, or an action to create one.
    // First try grabbing the actual mod-time of the file
    try {
      this.updateModTime();
    }
    // Then fall back to looking for an action
    catch(e) {
      if (typeof this.action == 'function') {
        return true;
      }
      else {
        throw new Error('File-task ' + this.fullName + ' has no ' +
          'existing file, and no action to create one.');
      }
    }

    // Compare mod-time of all the prereqs with its mod-time
    // If any prereqs are newer, need to run the action to update
    if (prereqs && prereqs.length) {
      for (var i = 0, ii = prereqs.length; i < ii; i++) {
        prereqName = prereqs[i];
        prereqTask = this.namespace.resolveTask(prereqName) ||
          jake.createPlaceholderFileTask(prereqName, this.namespace);
        // Run the action if:
        // 1. The prereq is a normal task (not file/dir)
        // 2. The prereq is a file-task with a mod-date more recent than
        // the one for this file/dir
        if (prereqTask) {
          if (!isFileOrDirectory(prereqTask) ||
              (isFile(prereqTask) && prereqTask.modTime > this.modTime)) {
            return true;
          }
        }
      }
    }
    // File/dir has no prereqs, and exists -- no need to run
    else {
      return false;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.FileTask.prototype.updateModTime"></a>[function <span class="apidocSignatureSpan">jake.FileTask.prototype.</span>updateModTime ()](#apidoc.element.jake.FileTask.prototype.updateModTime)
- description and source-code
```javascript
updateModTime = function () {
  var stats = fs.statSync(this.name);
  this.modTime = stats.mtime;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.Namespace"></a>[module jake.Namespace](#apidoc.module.jake.Namespace)

#### <a name="apidoc.element.jake.Namespace.Namespace"></a>[function <span class="apidocSignatureSpan">jake.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.Namespace.Namespace)
- description and source-code
```javascript
Namespace = function (name, parentNamespace) {
  this.name = name;
  this.parentNamespace = parentNamespace;
  this.childNamespaces = {};
  this.tasks = {};
  this.rules = {};
  this.path = this.getPath();
}
```
- example usage
```shell
...
    task('clobber', function () {
      // Clobber the doc directory first
    });
  });
 */
this.namespace = function (name, closure) {
  var curr = jake.currentNamespace
    , ns = curr.childNamespaces[name] || new jake.Namespace(name, curr);
  curr.childNamespaces[name] = ns;
  jake.currentNamespace = ns;
  closure();
  jake.currentNamespace = curr;
  jake.currentTaskDescription = null;
  return ns;
};
...
```



# <a name="apidoc.module.jake.Namespace.prototype"></a>[module jake.Namespace.prototype](#apidoc.module.jake.Namespace.prototype)

#### <a name="apidoc.element.jake.Namespace.prototype.getPath"></a>[function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>getPath ()](#apidoc.element.jake.Namespace.prototype.getPath)
- description and source-code
```javascript
getPath = function () {
  var parts = []
    , next = this;
  while (!!next) {
    parts.push(next.name);
    next = next.parentNamespace;
  }
  parts.pop(); // Remove 'default'
  return parts.reverse().join(':');
}
```
- example usage
```shell
...

var Namespace = function (name, parentNamespace) {
this.name = name;
this.parentNamespace = parentNamespace;
this.childNamespaces = {};
this.tasks = {};
this.rules = {};
this.path = this.getPath();
};

Namespace.prototype = new (function () {

this.resolveTask = function(relativeName) {
  var parts = relativeName.split(':')
    , name = parts.pop()
...
```

#### <a name="apidoc.element.jake.Namespace.prototype.matchRule"></a>[function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>matchRule (relativeName)](#apidoc.element.jake.Namespace.prototype.matchRule)
- description and source-code
```javascript
matchRule = function (relativeName) {
  var parts = relativeName.split(':')
    , name = parts.pop()
    , ns = this.resolveNamespace(parts.join(':'))
    , rules = ns ? ns.rules : []
    , r
    , match;

  for (var p in rules) {
    r = rules[p];
    if (r.match(relativeName)) {
      match = r;
    }
  }

  return (ns && match) ||
      (this.parentNamespace &&
      this.parentNamespace.matchRule(relativeName));
}
```
- example usage
```shell
...
    if (r.match(relativeName)) {
      match = r;
    }
  }

  return (ns && match) ||
      (this.parentNamespace &&
      this.parentNamespace.matchRule(relativeName));
};

this.getPath = function () {
  var parts = []
    , next = this;
  while (!!next) {
    parts.push(next.name);
...
```

#### <a name="apidoc.element.jake.Namespace.prototype.resolveNamespace"></a>[function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>resolveNamespace (relativeName)](#apidoc.element.jake.Namespace.prototype.resolveNamespace)
- description and source-code
```javascript
resolveNamespace = function (relativeName) {
  var parts = relativeName.split(':')
    , ns;

  if (!relativeName) {
    return this;
  }

  ns = this;
  for (var i = 0, ii = parts.length; ns && i < ii; i++) {
    ns = ns.childNamespaces[parts[i]];
  }

  return (ns || (this.parentNamespace &&
      this.parentNamespace.resolveNamespace(relativeName)));
}
```
- example usage
```shell
...
};

Namespace.prototype = new (function () {

this.resolveTask = function(relativeName) {
  var parts = relativeName.split(':')
    , name = parts.pop()
    , ns = this.resolveNamespace(parts.join(':'));

  return (ns && ns.tasks[name]) ||
      (this.parentNamespace &&
      this.parentNamespace.resolveTask(relativeName));
};

this.resolveNamespace = function(relativeName) {
...
```

#### <a name="apidoc.element.jake.Namespace.prototype.resolveTask"></a>[function <span class="apidocSignatureSpan">jake.Namespace.prototype.</span>resolveTask (relativeName)](#apidoc.element.jake.Namespace.prototype.resolveTask)
- description and source-code
```javascript
resolveTask = function (relativeName) {
  var parts = relativeName.split(':')
    , name = parts.pop()
    , ns = this.resolveNamespace(parts.join(':'));

  return (ns && ns.tasks[name]) ||
      (this.parentNamespace &&
      this.parentNamespace.resolveTask(relativeName));
}
```
- example usage
```shell
...
  this.resolveTask = function(relativeName) {
var parts = relativeName.split(':')
  , name = parts.pop()
  , ns = this.resolveNamespace(parts.join(':'));

return (ns && ns.tasks[name]) ||
    (this.parentNamespace &&
    this.parentNamespace.resolveTask(relativeName));
  };

  this.resolveNamespace = function(relativeName) {
var parts = relativeName.split(':')
  , ns;

if (!relativeName) {
...
```



# <a name="apidoc.module.jake.PackageTask"></a>[module jake.PackageTask](#apidoc.module.jake.PackageTask)

#### <a name="apidoc.element.jake.PackageTask.PackageTask"></a>[function <span class="apidocSignatureSpan">jake.</span>PackageTask ()](#apidoc.element.jake.PackageTask.PackageTask)
- description and source-code
```javascript
PackageTask = function () {
  var args = Array.prototype.slice.call(arguments)
    , name = args.shift()
    , version = args.shift()
    , definition = args.pop()
    , prereqs = args.pop() || []; // Optional

    prereqs = [].concat(prereqs); // Accept string or list

<span class="apidocCodeCommentSpan">  /**
    @name jake.PackageTask#name
    @public
    @type {String}
    @description The name of the project
   */
</span>  this.name = name;
  /**
    @name jake.PackageTask#version
    @public
    @type {String}
    @description The project version-string
   */
  this.version = version;
  /**
    @name jake.PackageTask#prereqs
    @public
    @type {Array}
    @description Tasks to run before packaging
   */
  this.prereqs = prereqs;
  /**
    @name jake.PackageTask#version
    @public
    @type {String='pkg'}
    @description The directory-name to use for packaging the software
   */
  this.packageDir = 'pkg';
  /**
    @name jake.PackageTask#packageFiles
    @public
    @type {jake.FileList}
    @description The list of files and directories to include in the
    package-archive
   */
  this.packageFiles = new FileList();
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tgz archive of the package
   */
  this.needTar = false;
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tar.gz archive of the package
   */
  this.needTarGz = false;
  /**
    @name jake.PackageTask#needTarBz2
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a bzip2 .bz2 archive of the package
   */
  this.needTarBz2 = false;
  /**
    @name jake.PackageTask#needJar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'jar' utility to create
    a .jar archive of the package
   */
  this.needJar = false;
  /**
    @name jake.PackageTask#needZip
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'zip' utility to create
    a .zip archive of the package
   */
  this.needZip = false;
  /**
    @name jake.PackageTask#manifestFile
    @public
    @type {String=null}
    @description Can be set to point the 'jar' utility at a manifest
    file to use in a .jar archive. If unset, one will be automatically
    created by the 'jar' utility. This path should be relative to the
    root of the package directory (this.packageDir above, likely 'pkg')
   */
  this.manifestFile = null;
  /**
    @name jake.PackageTask#tarCommand
    @public
    @type {String='tar'}
    @description The shell-command to use for creating tar archives.
   */
  this.tarCommand = 'tar';
  /**
    @name jake.PackageTask#jarCommand
    @public
    @type {String='jar'}
    @description The shell-command to use for creating jar archives.
   */
  this.jarCommand = 'jar';
  /**
    @name jake.PackageTask#zipCommand
    @public
    @type {String='zip'}
    @description The shell-command to use for creating zip archives.
   */
  this.zipCommand = 'zip';
  /**
    @name jake.PackageTask#archiveNoBaseDir
    @public
    @type {Boolean=false}
    @description Simple option for performing the archive on the
    contents of the directory instead of the directory itself
   */
  this.archiveNoBaseDir = false;
  /**
    @name jake.PackageTask#archiveChangeDir
    @public
    @type {String=null}
    @description Equivalent to the '-C' command for the 'tar' and 'jar'
    commands. ("Change to this directory before adding files.")
   */
  this.archiveChangeDir = null;
  /**
    @name jake.PackageTask#archiveContentDir
    @public
    @type {String=null}
    @description Specifies the files and directories to include in the
    package-archive. If unset, this will default to the main package
    directory -- i.e., name + version.
   */
  this.archiveContentDir = null;

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
  }
  else {
    throw new Error();
  }
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
...
```



# <a name="apidoc.module.jake.PackageTask.prototype"></a>[module jake.PackageTask.prototype](#apidoc.module.jake.PackageTask.prototype)

#### <a name="apidoc.element.jake.PackageTask.prototype.define"></a>[function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>define ()](#apidoc.element.jake.PackageTask.prototype.define)
- description and source-code
```javascript
define = function () {
  var self = this
    , packageDirPath = this.packageDirPath()
    , compressTaskArr = [];

  desc('Build the package for distribution');
  task('package', self.prereqs.concat(['clobberPackage', 'buildPackage']));
  // Backward-compat alias
  task('repackage', ['package']);

  task('clobberPackage', function () {
    jake.rmRf(self.packageDir, {silent: true});
  });

  desc('Remove the package');
  task('clobber', ['clobberPackage']);

  var doCommand = function (p) {
    var filename = path.resolve(self.packageDir + '/' + self.packageName() +
                                _compressOpts[p].ext);
    if (process.platform == 'win32') {
        // Windows full path may have drive letter, which is going to cause
        // namespace problems, so strip it.
        if (filename.length > 2 && filename[1] == ':') {
          filename = filename.substr(2);
        }
    }
    compressTaskArr.push(filename);

    file(filename, [packageDirPath], function () {
      var cmd
      , opts = _compressOpts[p]
      // Directory to move to when doing the compression-task
      // Changes in the case of zip for emulating -C option
      , chdir = self.packageDir
      // Save the current dir so it's possible to pop back up
      // after compressing
      , currDir = process.cwd()
      , archiveChangeDir
      , archiveContentDir;

      if (self.archiveNoBaseDir) {
        archiveChangeDir = self.packageName();
        archiveContentDir = '.';
      }
      else {
        archiveChangeDir = self.archiveChangeDir;
        archiveContentDir = self.archiveContentDir;
      }

      cmd = self[opts.cmd + 'Command'];
      cmd += ' -' + opts.flags;
      if (opts.cmd == 'jar' && self.manifestFile) {
        cmd += 'm';
      }

      // The name of the archive to create -- use full path
      // so compression can be performed from a different dir
      // if needed
      cmd += ' ' + filename;

      if (opts.cmd == 'jar' && self.manifestFile) {
        cmd += ' ' + self.manifestFile;
      }

      // Where to perform the compression -- -C option isn't
      // supported in zip, so actually do process.chdir for this
      if (archiveChangeDir) {
        if (opts.cmd == 'zip') {
          chdir = path.join(chdir, archiveChangeDir);
        }
        else {
          cmd += ' -C ' + archiveChangeDir;
        }
      }

      // Where to get the archive content
      if (archiveContentDir) {
        cmd += ' ' + archiveContentDir;
      }
      else {
        cmd += ' ' + self.packageName();
      }

      // Move into the desired dir (usually packageDir) to compress
      // Return back up to the current dir after the exec
      process.chdir(chdir);

      exec(cmd, function (err, stdout, stderr) {
        if (err) { throw err; }

        // Return back up to the starting directory (see above,
        // before exec)
        process.chdir(currDir);

        complete();
      });
    }, {async: true});
  };

  for (var p in _compressOpts) {
    if (this['need' + p]) {
      doCommand(p);
    }
  }

  task('buildPackage', compressTaskArr, function () {});

  directory(this.packageDir);

  file(packageDirPath, this.packageFiles, function () {
    jake.mkdirP(packageDirPath);
    var fileList = [];
    self.packageFiles.forEach(function (name) {
      var f = path.join(self.packageDirPath(), name)
        , fDir = path.dirname(f)
        , stats;
      jake.mkdirP(fDir, {silent: true});

      // Add both files and directories
      fileList.push({
        from: name
      , to: f
      });
    });
    var _copyFile = function () {
      var cmd
        , file = fileList.pop()
        , stat;
      if (file) {
        stat = fs.statSync(file.from);
        // Target is a directory, just create it
        if (stat.isDirectory()) {
          jake.mkdirP(file.to, {silent: true});
          _copyFile();
        }
        // Otherwise copy the file
        else {
          jake.cpR(file.from, file.to, {silent: true});
          _copyFile();
        }
      }
      else {
        complete();
      }
    };
    _copyFile();
  }, {asyn ...
```
- example usage
```shell
...
  directory -- i.e., name + version.
 */
this.archiveContentDir = null;

if (typeof definition == 'function') {
  definition.call(this);
}
this.define();
};

PackageTask.prototype = new (function () {

var _compressOpts = {
      Tar: {
        ext: '.tgz'
...
```

#### <a name="apidoc.element.jake.PackageTask.prototype.packageDirPath"></a>[function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>packageDirPath ()](#apidoc.element.jake.PackageTask.prototype.packageDirPath)
- description and source-code
```javascript
packageDirPath = function () {
  return this.packageDir + '/' + this.packageName();
}
```
- example usage
```shell
...
    , flags: 'qr'
    , cmd: 'zip'
    }
  };

  this.define = function () {
var self = this
  , packageDirPath = this.packageDirPath()
  , compressTaskArr = [];

desc('Build the package for distribution');
task('package', self.prereqs.concat(['clobberPackage', 'buildPackage']));
// Backward-compat alias
task('repackage', ['package']);
...
```

#### <a name="apidoc.element.jake.PackageTask.prototype.packageName"></a>[function <span class="apidocSignatureSpan">jake.PackageTask.prototype.</span>packageName ()](#apidoc.element.jake.PackageTask.prototype.packageName)
- description and source-code
```javascript
packageName = function () {
  if (this.version) {
    return this.name + '-' + this.version;
  }
  else {
    return this.name;
  }
}
```
- example usage
```shell
...
  jake.rmRf(self.packageDir, {silent: true});
});

desc('Remove the package');
task('clobber', ['clobberPackage']);

var doCommand = function (p) {
  var filename = path.resolve(self.packageDir + '/' + self.packageName() +
                              _compressOpts[p].ext);
  if (process.platform == 'win32') {
      // Windows full path may have drive letter, which is going to cause
      // namespace problems, so strip it.
      if (filename.length > 2 && filename[1] == ':') {
        filename = filename.substr(2);
      }
...
```



# <a name="apidoc.module.jake.PublishTask"></a>[module jake.PublishTask](#apidoc.module.jake.PublishTask)

#### <a name="apidoc.element.jake.PublishTask.PublishTask"></a>[function <span class="apidocSignatureSpan">jake.</span>PublishTask ()](#apidoc.element.jake.PublishTask.PublishTask)
- description and source-code
```javascript
PublishTask = function () {
  var args = Array.prototype.slice.call(arguments).filter(function (item) {
        return typeof item != 'undefined';
      })
    , arg
    , opts = {}
    , definition
    , prereqs = []
    , createDef = function (arg) {
        return function () {
          this.packageFiles.include(arg);
        };
      };

  this.name = args.shift();

  // Old API, just name + list of files
  if (args.length == 1 && (Array.isArray(args[0]) || typeof args[0] == 'string')) {
    definition = createDef(args.pop());
  }
  // Current API, name + [prereqs] + [opts] + definition
  else {
    while ((arg = args.pop())) {
      // Definition func
      if (typeof arg == 'function') {
        definition = arg;
      }
      // Prereqs
      else if (Array.isArray(arg) || typeof arg == 'string') {
        prereqs = arg;
      }
      // Opts
      else {
        opts = arg;
      }
    }
  }

  this.prereqs = prereqs;
  this.packageFiles = new FileList();
  this.publishCmd = opts.publishCmd || 'npm publish %filename';
  this.publishMessage = opts.publishMessage || 'BOOM! Published.';
  this.gitCmd = opts.gitCmd || 'git';
  this.versionFiles = opts.versionFiles || ['package.json'];
  this.scheduleDelay = 5000;

  // Override utility funcs for testing
  this._ensureRepoClean = function (stdout) {
    if (stdout.length) {
      fail(new Error('Git repository is not clean.'));
    }
  };
  this._getCurrentBranch = function (stdout) {
    return utils.string.trim(stdout);
  };

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
this.npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};
...
```



# <a name="apidoc.module.jake.PublishTask.prototype"></a>[module jake.PublishTask.prototype](#apidoc.module.jake.PublishTask.prototype)

#### <a name="apidoc.element.jake.PublishTask.prototype.define"></a>[function <span class="apidocSignatureSpan">jake.PublishTask.prototype.</span>define ()](#apidoc.element.jake.PublishTask.prototype.define)
- description and source-code
```javascript
define = function () {
  var self = this;

  namespace('publish', function () {
    task('fetchTags', {async: true}, function () {
      // Make sure local tags are up to date
      var cmds = [
        self.gitCmd + ' fetch --tags'
      ];
      jake.exec(cmds, function () {
        console.log('Fetched remote tags.');
        complete();
      });
    });

    task('getCurrentBranch', {async: true}, function () {
      // Figure out what branch to push to
      exec(self.gitCmd + ' symbolic-ref --short HEAD',
          function (err, stdout, stderr) {
        if (err) {
          fail(err);
        }
        if (stderr) {
          fail(new Error(stderr));
        }
        if (!stdout) {
          fail(new Error('No current Git branch found'));
        }
        _currentBranch = self._getCurrentBranch(stdout);
        console.log('On branch ' + _currentBranch);
        complete();
      });
    });

    task('ensureClean', {async: true}, function () {
      // Only bump, push, and tag if the Git repo is clean
      exec(self.gitCmd + ' status --porcelain --untracked-files=no',
          function (err, stdout, stderr) {
        if (err) {
          fail(err);
        }
        if (stderr) {
          fail(new Error(stderr));
        }

        // Throw if there's output
        self._ensureRepoClean(stdout);

        complete();
      });
    });

    task('updateVersionFiles', function () {
      var pkg
        , version
        , arr
        , patch;

      // Grab the current version-string
      pkg = getPackage();
      version = pkg.version;
      // Increment the patch-number for the version
      arr = version.split('.');
      patch = parseInt(arr.pop(), 10) + 1;
      arr.push(patch);
      version = arr.join('.');

      // Update package.json or other files with the new version-info
      self.versionFiles.forEach(function (file) {
        var p = path.join(process.cwd(), file)
          , data = JSON.parse(fs.readFileSync(p).toString());
        data.version = version;
        fs.writeFileSync(p, JSON.stringify(data, true, 2) + '\n');
      });
      // Return the version string so that listeners for the 'complete' event
      // for this task can use it (e.g., to update other files before pushing
      // to Git)
      return version;
    });

    task('pushVersion', ['ensureClean', 'updateVersionFiles'], {async: true},
        function () {
      var version = getPackageVersionNumber()
        , message = 'Version ' + version
        , cmds = [
            self.gitCmd + ' commit -a -m "' + message + '"'
          , self.gitCmd + ' push origin ' + _currentBranch
          , self.gitCmd + ' tag -a v' + version + ' -m "' + message + '"'
          , self.gitCmd + ' push --tags'
          ];

      var execOpts = {};
      if (process.platform == 'win32') {
        // Windows won't like the quotes in our cmdline
        execOpts.windowsVerbatimArguments = true;
      }

      jake.exec(cmds, function () {
        var version = getPackageVersionNumber();
        console.log('Bumped version number to v' + version + '.');
        complete();
      }, execOpts);

    });

    task('definePackage', function () {
      var version = getPackageVersionNumber()
        , t;
      t = new jake.PackageTask(self.name, 'v' + version, self.prereqs, function () {
        // Replace the PackageTask's FileList with the PublishTask's FileList
        this.packageFiles = self.packageFiles;
        this.needTarGz = true; // Default to tar.gz
        // If any of the need<CompressionFormat> or archive opts are set
        // proxy them to the PackageTask
        for (var p in this) {
          if (p.indexOf('need') === 0 || p.indexOf('archive') === 0) {
            if (typeof self[p] != 'undefined') {
              this[p] = self[p];
            }
          }
        }
      });
    });

    task('package', {async: true}, function () {
      var definePack = jake.Task['publish:definePackage']
        , pack = jake.Task.package
        , version = getPackageVersionNumber();

      // May have already been run
      definePack.reenable(tr ...
```
- example usage
```shell
...
  directory -- i.e., name + version.
 */
this.archiveContentDir = null;

if (typeof definition == 'function') {
  definition.call(this);
}
this.define();
};

PackageTask.prototype = new (function () {

var _compressOpts = {
      Tar: {
        ext: '.tgz'
...
```



# <a name="apidoc.module.jake.Rule"></a>[module jake.Rule](#apidoc.module.jake.Rule)

#### <a name="apidoc.element.jake.Rule.Rule"></a>[function <span class="apidocSignatureSpan">jake.</span>Rule (opts)](#apidoc.element.jake.Rule.Rule)
- description and source-code
```javascript
Rule = function (opts) {
  this.pattern = opts.pattern;
  this.source = opts.source;
  this.prereqs = opts.prereqs;
  this.action = opts.action;
  this.opts = opts.opts;
  this.desc =  opts.desc;
  this.ns = opts.ns;
}
```
- example usage
```shell
...
    prereqs = arg;
  }
  else {
    opts = arg;
  }
}

jake.currentNamespace.rules[key] = new jake.Rule({
  pattern: pattern
, source: source
, prereqs: prereqs
, action: action
, opts: opts
, desc: jake.currentTaskDescription
, ns: jake.currentNamespace
...
```



# <a name="apidoc.module.jake.Rule.prototype"></a>[module jake.Rule.prototype](#apidoc.module.jake.Rule.prototype)

#### <a name="apidoc.element.jake.Rule.prototype.createTask"></a>[function <span class="apidocSignatureSpan">jake.Rule.prototype.</span>createTask (fullName, level)](#apidoc.element.jake.Rule.prototype.createTask)
- description and source-code
```javascript
createTask = function (fullName, level) {
  var self = this
    , pattern
    , source
    , action
    , opts
    , prereqs
    , parts
    , valid
    , src
    , tNs
    , createdTask
    , name = Task.getBaseTaskName(fullName)
    , nsPath = Task.getBaseNamespacePath(fullName)
    , ns = this.ns.resolveNamespace(nsPath);

  pattern = this.pattern;
  source = this.source;

  if (typeof source == 'string') {
    src = Matcher.getSource(name, pattern, source);
  }
  else {
    src = source(name);
  }

  // TODO: Write a utility function that appends a
  // taskname to a namespace path
  src = nsPath.split(':').filter(function (item) {
    return !!item;
  }).concat(src).join(':');

  // Generate the prerequisite for the matching task.
  //    It is the original prerequisites plus the prerequisite
  //    representing source file, i.e.,
  //
  //      rule( '%.o', '%.c', ['some.h'] ...
  //
  //    If the objective is main.o, then new task should be
  //
  //      file( 'main.o', ['main.c', 'some.h' ] ...
  prereqs = this.prereqs.slice(); // Get a copy to work with
  prereqs.unshift(src);

  // Prereq should be:
  // 1. an existing task
  // 2. an existing file on disk
  // 3. a valid rule (i.e., not at too deep a level)
  valid = prereqs.some(function (p) {
    var ns = self.ns;
    return ns.resolveTask(p) ||
      fs.existsSync(Task.getBaseTaskName(p)) ||
      jake.attemptRule(p, ns, level + 1);
  });

  // If any of the prereqs aren't valid, the rule isn't valid
  if (!valid) {
    return null;
  }
  // Otherwise, hunky-dory, finish creating the task for the rule
  else {
    // Create the action for the task
    action = function () {
      var task = this;
      self.action.apply(task);
    };

    opts = this.opts;

    // Insert the file task into Jake
    //
    // Since createTask function stores the task as a child task
    // of currentNamespace. Here we temporariliy switch the namespace.
    // FIXME: Should allow optional ns passed in instead of this hack
    tNs = jake.currentNamespace;
    jake.currentNamespace = ns;
    createdTask = jake.createTask('file', name, prereqs, action, opts);
    createdTask.source = src.split(':').pop();
    jake.currentNamespace = tNs;

    return createdTask;
  }

}
```
- example usage
```shell
...
    // Insert the file task into Jake
    //
    // Since createTask function stores the task as a child task
    // of currentNamespace. Here we temporariliy switch the namespace.
    // FIXME: Should allow optional ns passed in instead of this hack
    tNs = jake.currentNamespace;
    jake.currentNamespace = ns;
    createdTask = jake.createTask('file', name, prereqs, action, opts);
    createdTask.source = src.split(':').pop();
    jake.currentNamespace = tNs;

    return createdTask;
  }

};
...
```

#### <a name="apidoc.element.jake.Rule.prototype.match"></a>[function <span class="apidocSignatureSpan">jake.Rule.prototype.</span>match (name)](#apidoc.element.jake.Rule.prototype.match)
- description and source-code
```javascript
match = function (name) {
  return Matcher.match(this.pattern, name);
}
```
- example usage
```shell
...
  , ns = this.resolveNamespace(parts.join(':'))
  , rules = ns ? ns.rules : []
  , r
  , match;

for (var p in rules) {
  r = rules[p];
  if (r.match(relativeName)) {
    match = r;
  }
}

return (ns && match) ||
    (this.parentNamespace &&
    this.parentNamespace.matchRule(relativeName));
...
```



# <a name="apidoc.module.jake.SortedCollection"></a>[module jake.SortedCollection](#apidoc.module.jake.SortedCollection)

#### <a name="apidoc.element.jake.SortedCollection.SortedCollection"></a>[function <span class="apidocSignatureSpan">jake.</span>SortedCollection (d)](#apidoc.element.jake.SortedCollection.SortedCollection)
- description and source-code
```javascript
SortedCollection = function (d) {
  this.count = 0;
  this.items = {}; // Hash keys and their values
  this.order = []; // Array for sort order
  if (d) {
    this.defaultValue = d;
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.SortedCollection.prototype"></a>[module jake.SortedCollection.prototype](#apidoc.module.jake.SortedCollection.prototype)

#### <a name="apidoc.element.jake.SortedCollection.prototype.addItem"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>addItem (key, val)](#apidoc.element.jake.SortedCollection.prototype.addItem)
- description and source-code
```javascript
addItem = function (key, val) {
  if (typeof key != 'string') {
    throw('Hash only allows string keys.');
  }
  return this.setByKey(key, val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.allKeys"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>allKeys (str)](#apidoc.element.jake.SortedCollection.prototype.allKeys)
- description and source-code
```javascript
allKeys = function (str) {
  return this.order.join(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.clone"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>clone ()](#apidoc.element.jake.SortedCollection.prototype.clone)
- description and source-code
```javascript
clone = function () {
  var coll = new SortedCollection()
    , key
    , val;
  for (var i = 0; i < this.order.length; i++) {
    key = this.order[i];
    val = this.items[key];
    coll.setItem(key, val);
  }
  return coll;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.concat"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>concat (hNew)](#apidoc.element.jake.SortedCollection.prototype.concat)
- description and source-code
```javascript
concat = function (hNew) {
  for (var i = 0; i < hNew.order.length; i++) {
    var key = hNew.order[i];
    var val = hNew.items[key];
    this.setItem(key, val);
  }
}
```
- example usage
```shell
...
var PackageTask = function () {
var args = Array.prototype.slice.call(arguments)
  , name = args.shift()
  , version = args.shift()
  , definition = args.pop()
  , prereqs = args.pop() || []; // Optional

  prereqs = [].concat(prereqs); // Accept string or list

/**
  @name jake.PackageTask#name
  @public
  @type {String}
  @description The name of the project
 */
...
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.each"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>each (func, opts)](#apidoc.element.jake.SortedCollection.prototype.each)
- description and source-code
```javascript
each = function (func, opts) {
  var options = opts || {}
    , order = this.order;
  for (var i = 0, ii = order.length; i < ii; i++) {
    var key = order[i];
    var val = this.items[key];
    if (options.keyOnly) {
      func(key);
    }
    else if (options.valueOnly) {
      func(val);
    }
    else {
      func(val, key);
    }
  }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.eachKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>eachKey (func)](#apidoc.element.jake.SortedCollection.prototype.eachKey)
- description and source-code
```javascript
eachKey = function (func) {
  return this.each(func, { keyOnly: true });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.eachValue"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>eachValue (func)](#apidoc.element.jake.SortedCollection.prototype.eachValue)
- description and source-code
```javascript
eachValue = function (func) {
  return this.each(func, { valueOnly: true });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.getByIndex"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getByIndex (ind)](#apidoc.element.jake.SortedCollection.prototype.getByIndex)
- description and source-code
```javascript
getByIndex = function (ind) {
  return this.items[this.order[ind]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.getByKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getByKey (key)](#apidoc.element.jake.SortedCollection.prototype.getByKey)
- description and source-code
```javascript
getByKey = function (key) {
  return this.items[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.getItem"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getItem (p)](#apidoc.element.jake.SortedCollection.prototype.getItem)
- description and source-code
```javascript
getItem = function (p) {
  if (typeof p == 'string') {
    return this.getByKey(p);
  }
  else if (typeof p == 'number') {
    return this.getByIndex(p);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.getPosition"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>getPosition (key)](#apidoc.element.jake.SortedCollection.prototype.getPosition)
- description and source-code
```javascript
getPosition = function (key) {
  var order = this.order;
  if (typeof order.indexOf == 'function') {
    return order.indexOf(key);
  }
  else {
    for (var i = 0; i < order.length; i++) {
      if (order[i] == key) { return i;}
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.hasKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>hasKey (key)](#apidoc.element.jake.SortedCollection.prototype.hasKey)
- description and source-code
```javascript
hasKey = function (key) {
  return typeof this.items[key] != 'undefined';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.hasValue"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>hasValue (val)](#apidoc.element.jake.SortedCollection.prototype.hasValue)
- description and source-code
```javascript
hasValue = function (val) {
  for (var i = 0; i < this.order.length; i++) {
    if (this.items[this.order[i]] == val) {
      return true;
    }
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.insertAfterKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>insertAfterKey (refKey, key, val)](#apidoc.element.jake.SortedCollection.prototype.insertAfterKey)
- description and source-code
```javascript
insertAfterKey = function (refKey, key, val) {
  var pos = this.getPosition(refKey);
  return this.insertAtIndex(pos, key, val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.insertAtIndex"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>insertAtIndex (ind, key, val)](#apidoc.element.jake.SortedCollection.prototype.insertAtIndex)
- description and source-code
```javascript
insertAtIndex = function (ind, key, val) {
  this.order.splice(ind, 0, key);
  this.items[key] = val;
  this.count++;
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.pop"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>pop ()](#apidoc.element.jake.SortedCollection.prototype.pop)
- description and source-code
```javascript
pop = function () {
  var pos = this.count-1;
  var ret = this.items[this.order[pos]];
  if (typeof ret != 'undefined') {
    this.removeByIndex(pos);
    return ret;
  }
  else {
    return;
  }
}
```
- example usage
```shell
...
this.path = this.getPath();
};

Namespace.prototype = new (function () {

this.resolveTask = function(relativeName) {
  var parts = relativeName.split(':')
    , name = parts.pop()
    , ns = this.resolveNamespace(parts.join(':'));

  return (ns && ns.tasks[name]) ||
      (this.parentNamespace &&
      this.parentNamespace.resolveTask(relativeName));
};
...
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.push"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>push (key, val)](#apidoc.element.jake.SortedCollection.prototype.push)
- description and source-code
```javascript
push = function (key, val) {
  this.insertAtIndex(this.count, key, val);
  return this.count;
}
```
- example usage
```shell
...
        this.parentNamespace.matchRule(relativeName));
  };

  this.getPath = function () {
    var parts = []
      , next = this;
    while (!!next) {
      parts.push(next.name);
      next = next.parentNamespace;
    }
    parts.pop(); // Remove 'default'
    return parts.reverse().join(':');
  };

})();
...
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.removeByIndex"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeByIndex (ind)](#apidoc.element.jake.SortedCollection.prototype.removeByIndex)
- description and source-code
```javascript
removeByIndex = function (ind) {
  var ret = this.items[this.order[ind]];
  if (typeof ret != 'undefined') {
    delete this.items[this.order[ind]]
    this.order.splice(ind, 1);
    this.count--;
    return true;
  }
  else {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.removeByKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeByKey (key)](#apidoc.element.jake.SortedCollection.prototype.removeByKey)
- description and source-code
```javascript
removeByKey = function (key) {
  if (typeof this.items[key] != 'undefined') {
    var pos = null;
    delete this.items[key]; // Remove the value
    // Find the key in the order list
    for (var i = 0; i < this.order.length; i++) {
      if (this.order[i] == key) {
        pos = i;
      }
    }
    this.order.splice(pos, 1); // Remove the key
    this.count--; // Decrement the length
    return true;
  }
  else {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.removeItem"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>removeItem (p)](#apidoc.element.jake.SortedCollection.prototype.removeItem)
- description and source-code
```javascript
removeItem = function (p) {
  if (typeof p == 'string') {
    return this.removeByKey(p);
  }
  else if (typeof p == 'number') {
    return this.removeByIndex(p);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.replaceKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>replaceKey (oldKey, newKey)](#apidoc.element.jake.SortedCollection.prototype.replaceKey)
- description and source-code
```javascript
replaceKey = function (oldKey, newKey) {
  // If item for newKey exists, nuke it
  if (this.hasKey(newKey)) {
    this.removeItem(newKey);
  }
  this.items[newKey] = this.items[oldKey];
  delete this.items[oldKey];
  for (var i = 0; i < this.order.length; i++) {
    if (this.order[i] == oldKey) {
      this.order[i] = newKey;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.reverse"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>reverse ()](#apidoc.element.jake.SortedCollection.prototype.reverse)
- description and source-code
```javascript
reverse = function () {
  this.order.reverse();
}
```
- example usage
```shell
...
    var parts = []
      , next = this;
    while (!!next) {
      parts.push(next.name);
      next = next.parentNamespace;
    }
    parts.pop(); // Remove 'default'
    return parts.reverse().join(':');
  };

})();

module.exports.Namespace = Namespace;
...
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.setByIndex"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setByIndex (ind, val)](#apidoc.element.jake.SortedCollection.prototype.setByIndex)
- description and source-code
```javascript
setByIndex = function (ind, val) {
  if (ind < 0 || ind >= this.count) {
    throw('Index out of bounds. Hash length is ' + this.count);
  }
  this.items[this.order[ind]] = val;
  return this.items[this.order[ind]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.setByKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setByKey (key, val)](#apidoc.element.jake.SortedCollection.prototype.setByKey)
- description and source-code
```javascript
setByKey = function (key, val) {
  var v = null;
  if (typeof val == 'undefined') {
    v = this.defaultValue;
  }
  else { v = val; }
  if (typeof this.items[key] == 'undefined') {
    this.order[this.count] = key;
    this.count++;
  }
  this.items[key] = v;
  return this.items[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.setItem"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>setItem (p, val)](#apidoc.element.jake.SortedCollection.prototype.setItem)
- description and source-code
```javascript
setItem = function (p, val) {
  if (typeof p == 'string') {
    return this.setByKey(p, val);
  }
  else if (typeof p == 'number') {
    return this.setByIndex(p, val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.shift"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>shift ()](#apidoc.element.jake.SortedCollection.prototype.shift)
- description and source-code
```javascript
shift = function () {
  var pos = 0;
  var ret = this.items[this.order[pos]];
  if (typeof ret != 'undefined') {
    this.removeByIndex(pos);
    return ret;
  }
  else {
    return;
  }
}
```
- example usage
```shell
...
    // ...
  });
}
   */
  this.rule = function () {
var args = Array.prototype.slice.call(arguments)
  , arg
  , pattern = args.shift()
  , source = args.shift()
  , prereqs = []
  , action = function () {}
  , opts = {}
  , key = pattern.toString(); // May be a RegExp

while ((arg = args.shift())) {
...
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.sort"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>sort (c)](#apidoc.element.jake.SortedCollection.prototype.sort)
- description and source-code
```javascript
sort = function (c) {
  var arr = [];
  // Assumes vals are comparable scalars
  var comp = function (a, b) {
    return c(a.val, b.val);
  }
  for (var i = 0; i < this.order.length; i++) {
    var key = this.order[i];
    arr[i] = { key: key, val: this.items[key] };
  }
  arr.sort(comp);
  this.order = [];
  for (var i = 0; i < arr.length; i++) {
    this.order.push(arr[i].key);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.sortByKey"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>sortByKey (comp)](#apidoc.element.jake.SortedCollection.prototype.sortByKey)
- description and source-code
```javascript
sortByKey = function (comp) {
  this.order.sort(comp);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.splice"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>splice (index, numToRemove, hash)](#apidoc.element.jake.SortedCollection.prototype.splice)
- description and source-code
```javascript
splice = function (index, numToRemove, hash) {
  var _this = this;
  // Removal
  if (numToRemove > 0) {
    // Items
    var limit = index + numToRemove;
    for (var i = index; i < limit; i++) {
      delete this.items[this.order[i]];
    }
    // Order
    this.order.splice(index, numToRemove);
  }
  // Adding
  if (hash) {
    // Items
    for (var i in hash.items) {
      this.items[i] = hash.items[i];
    }
    // Order
    var args = hash.order;
    args.unshift(0);
    args.unshift(index);
    this.order.splice.apply(this.order, args);
  }
  this.count = this.order.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.SortedCollection.prototype.unshift"></a>[function <span class="apidocSignatureSpan">jake.SortedCollection.prototype.</span>unshift (key, val)](#apidoc.element.jake.SortedCollection.prototype.unshift)
- description and source-code
```javascript
unshift = function (key, val) {
  this.insertAtIndex(0, key, val);
  return this.count;
}
```
- example usage
```shell
...
    setTimeout(complete, 1000);
  }, {async: true});
 */
this.task = function (name, prereqs, action, opts) {
  var args = Array.prototype.slice.call(arguments)
    , type
    , createdTask;
  args.unshift('task');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
};

/**
  @name rule
...
```



# <a name="apidoc.module.jake.Task"></a>[module jake.Task](#apidoc.module.jake.Task)

#### <a name="apidoc.element.jake.Task.Task"></a>[function <span class="apidocSignatureSpan">jake.</span>Task ()](#apidoc.element.jake.Task.Task)
- description and source-code
```javascript
Task = function () {
  // Do constructor-work only on actual instances, not when used
  // for inheritance
  if (arguments.length) {
    this.init.apply(this, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.getBaseNamespacePath"></a>[function <span class="apidocSignatureSpan">jake.Task.</span>getBaseNamespacePath (fullName)](#apidoc.element.jake.Task.getBaseNamespacePath)
- description and source-code
```javascript
getBaseNamespacePath = function (fullName) {
  return fullName.split(':').slice(0, -1).join(':');
}
```
- example usage
```shell
...
  , prereqs
  , parts
  , valid
  , src
  , tNs
  , createdTask
  , name = Task.getBaseTaskName(fullName)
  , nsPath = Task.getBaseNamespacePath(fullName)
  , ns = this.ns.resolveNamespace(nsPath);

pattern = this.pattern;
source = this.source;

if (typeof source == 'string') {
  src = Matcher.getSource(name, pattern, source);
...
```

#### <a name="apidoc.element.jake.Task.getBaseTaskName"></a>[function <span class="apidocSignatureSpan">jake.Task.</span>getBaseTaskName (fullName)](#apidoc.element.jake.Task.getBaseTaskName)
- description and source-code
```javascript
getBaseTaskName = function (fullName) {
  return fullName.split(':').pop();
}
```
- example usage
```shell
...
  , opts
  , prereqs
  , parts
  , valid
  , src
  , tNs
  , createdTask
  , name = Task.getBaseTaskName(fullName)
  , nsPath = Task.getBaseNamespacePath(fullName)
  , ns = this.ns.resolveNamespace(nsPath);

pattern = this.pattern;
source = this.source;

if (typeof source == 'string') {
...
```

#### <a name="apidoc.element.jake.Task.super_"></a>[function <span class="apidocSignatureSpan">jake.Task.</span>super_ ()](#apidoc.element.jake.Task.super_)
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



# <a name="apidoc.module.jake.Task.prototype"></a>[module jake.Task.prototype](#apidoc.module.jake.Task.prototype)

#### <a name="apidoc.element.jake.Task.prototype.complete"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>complete (val)](#apidoc.element.jake.Task.prototype.complete)
- description and source-code
```javascript
complete = function (val) {
  jake._invocationChain.splice(jake._invocationChain.indexOf(this),1);

  this._currentPrereqIndex = 0;
  this.taskStatus = Task.runStatuses.DONE;

  // If 'complete' getting called because task has been
  // run already, value will not be passed -- leave in place
  if (typeof val != 'undefined') {
    this.value = val;
  }

  this.emit('complete', this.value);
}
```
- example usage
```shell
...
@static
@function
@description Completes an asynchronous task, allowing Jake's
execution to proceed to the next task. Calling complete globally or without
arguments completes the last task on the invocationChain. If you use parallel
execution of prereqs this will probably complete a wrong task. You should call this
function with this task as the first argument, before the optional return value.
Alternatively you can call task.complete()
'
@example
task('generate', ['doc:clobber'], function () {
  exec('./generate_docs.sh', function (err, stdout, stderr) {
    if (err || stderr) {
      fail(err || stderr);
    }
...
```

#### <a name="apidoc.element.jake.Task.prototype.execute"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>execute ()](#apidoc.element.jake.Task.prototype.execute)
- description and source-code
```javascript
execute = function () {
  jake._invocationChain.push(this);
  this.args = Array.prototype.slice.call(arguments);
  this.reenable();
  this.run();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.handlePrereqComplete"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>handlePrereqComplete (prereq)](#apidoc.element.jake.Task.prototype.handlePrereqComplete)
- description and source-code
```javascript
handlePrereqComplete = function (prereq) {
  var self = this;
  this._currentPrereqIndex++;
  if (this._currentPrereqIndex < this.prereqs.length) {
    process.nextTick(function () {
      self.nextPrereq();
    });
  }
  else {
    this.run();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.init"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>init (name, prereqs, action, options)](#apidoc.element.jake.Task.prototype.init)
- description and source-code
```javascript
init = function (name, prereqs, action, options) {
  var opts = options || {};

  this._currentPrereqIndex = 0;

  this.name = name;
  this.prereqs = prereqs;
  this.action = action;
  this.async = false;
  this.taskStatus = Task.runStatuses.UNSTARTED;
  this.fullName = null;
  this.description = null;
  this.args = [];
  this.value = UNDEFINED_VALUE;
  this.namespace = null;
  this.parallelLimit = 1;

  // Support legacy async-flag -- if not explicitly passed or falsy, will
  // be set to empty-object
  if (typeof opts == 'boolean' && opts === true) {
    this.async = true;
  }
  else {
    if (opts.async) {
      this.async = true;
    }
    if (opts.parallelLimit) {
      this.parallelLimit = opts.parallelLimit;
    }
  }

  //Do a test on self dependencies for this task
  if(Array.isArray(this.prereqs) && this.prereqs.indexOf(this.name) !== -1) {
    throw new Error("Cannot use prereq " + this.name + " as a dependency of itself");
  }

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.invoke"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>invoke ()](#apidoc.element.jake.Task.prototype.invoke)
- description and source-code
```javascript
invoke = function () {
  jake._invocationChain.push(this);
  this.args = Array.prototype.slice.call(arguments);
  this.runPrereqs();
}
```
- example usage
```shell
...
  task('__root__', taskNames, function () {});

  rootTask = jake.Task.__root__;
  rootTask.once('complete', function () {
    jake.emit('complete');
  });
  jake.emit('start');
  rootTask.invoke();
};

})();

die = function (msg) {
console.log(msg);
process.stdout.write('', function() {
...
```

#### <a name="apidoc.element.jake.Task.prototype.isNeeded"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>isNeeded ()](#apidoc.element.jake.Task.prototype.isNeeded)
- description and source-code
```javascript
isNeeded = function () {
  if (this.taskStatus === Task.runStatuses.DONE || typeof this.action != 'function') {
    return false;
  }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.nextPrereq"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>nextPrereq ()](#apidoc.element.jake.Task.prototype.nextPrereq)
- description and source-code
```javascript
nextPrereq = function () {
  var self = this
    , index = this._currentPrereqIndex
    , name = this.prereqs[index]
    , prereq
    , parsed
    , filePath
    , stats;

  if (name) {

    parsed = parsePrereqName(name);

    prereq = this.namespace.resolveTask(parsed.name) ||
        jake.attemptRule(name, this.namespace, 0) ||
        jake.createPlaceholderFileTask(name, this.namespace);

    if (!prereq) {
      throw new Error('Unknown task "' + name + '"');
    }

    // Do when done
    if (prereq.taskStatus === Task.runStatuses.DONE) {
      self.handlePrereqComplete(prereq);
    } else {
      prereq.once('complete', function () {
        self.handlePrereqComplete(prereq);
      });
      if(prereq.taskStatus === Task.runStatuses.UNSTARTED) {
         prereq.taskStatus = Task.runStatuses.STARTED;
         prereq.invoke.apply(prereq, parsed.args);
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.reenable"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>reenable (deep)](#apidoc.element.jake.Task.prototype.reenable)
- description and source-code
```javascript
reenable = function (deep) {
  var prereqs
    , prereq;
  this.taskStatus = Task.runStatuses.UNSTARTED;
  this.value = UNDEFINED_VALUE;
  if (deep && this.prereqs) {
    prereqs = this.prereqs;
    for (var i = 0, ii = prereqs.length; i < ii; i++) {
      prereq = jake.Task[prereqs[i]];
      if (prereq) {
        prereq.reenable(deep);
      }
    }
  }
}
```
- example usage
```shell
...

      task('package', {async: true}, function () {
var definePack = jake.Task['publish:definePackage']
  , pack = jake.Task.package
  , version = getPackageVersionNumber();

// May have already been run
definePack.reenable(true);
definePack.addListener('complete', function () {
  pack.addListener('complete', function () {
    console.log('Created package for ' + self.name + ' v' + version);
    complete();
  });
  pack.invoke();
});
...
```

#### <a name="apidoc.element.jake.Task.prototype.run"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>run ()](#apidoc.element.jake.Task.prototype.run)
- description and source-code
```javascript
run = function () {
  var runAction = this.isNeeded()
    , val;

  if (runAction) {
    this.emit('start');
    try {
      val = this.action.apply(this, this.args);

      if (typeof val == 'object' && typeof val.then == 'function') {
        this.async = true;

        val.then(
          function(result) {
            process.nextTick(function() {
                complete(result);
              });
          },
          function(err) {
            process.nextTick(function() {
                fail(err);
              });
          });
      }
    }
    catch (e) {
      this.emit('error', e);
      return; // Bail out, not complete
    }
  }
  else {
    this.emit('skip');
  }

  if (!(runAction && this.async)) {
    this.complete(val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.Task.prototype.runPrereqs"></a>[function <span class="apidocSignatureSpan">jake.Task.prototype.</span>runPrereqs ()](#apidoc.element.jake.Task.prototype.runPrereqs)
- description and source-code
```javascript
runPrereqs = function () {
  if (this.prereqs && this.prereqs.length) {
    if(this.parallelLimit > 1) {
      var currenttask = this;
      async.eachLimit(currenttask.prereqs,currenttask.parallelLimit,function(name, cb) {

        var parsed = parsePrereqName(name);

        var prereq = currenttask.namespace.resolveTask(parsed.name) ||
        jake.attemptRule(name, currenttask.namespace, 0) ||
        jake.createPlaceholderFileTask(name, currenttask.namespace);

        if (!prereq) {
          throw new Error('Unknown task "' + name + '"');
        }

        //Test for circular invocation
        if(prereq === currenttask) {
          cb(new Error("Cannot use prereq " + prereq.name + " as a dependency of itself"));
        }

        if (prereq.taskStatus === Task.runStatuses.DONE) {
          //prereq already done, return
          cb();
        } else {
          //wait for complete before calling cb
          prereq.once('complete', function () {
            cb();
          });
          //start te prereq if we are the first to encounter it
          if(prereq.taskStatus === Task.runStatuses.UNSTARTED) {
            prereq.taskStatus = Task.runStatuses.STARTED;
            prereq.invoke.apply(prereq, parsed.args);
          }
        }
      }, function(err) {
        //async callback is called after all prereqs have run.
        if(err) {
          throw err;
        } else {
          currenttask.run();
        }
      });
    } else {
      this.nextPrereq();
    }
  }
  else {
    this.run();
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.XML"></a>[module jake.XML](#apidoc.module.jake.XML)

#### <a name="apidoc.element.jake.XML.setIndentLevel"></a>[function <span class="apidocSignatureSpan">jake.XML.</span>setIndentLevel (level)](#apidoc.element.jake.XML.setIndentLevel)
- description and source-code
```javascript
setIndentLevel = function (level) {
  if(!level) {
    return;
  }

  return indentLevel = level;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.XML.stringify"></a>[function <span class="apidocSignatureSpan">jake.XML.</span>stringify (obj, opts)](#apidoc.element.jake.XML.stringify)
- description and source-code
```javascript
stringify = function (obj, opts) {
  var config = core.mixin({}, this.config)
    , xml = '';
  core.mixin(config, (opts || {}));

  if (!config.whitespace) {
    indentLevel = 0;
  }

  if (!config.fragment) {
    xml += '<?xml version="1.0" encoding="UTF-8"?>\n';
  }

  xml += obj2xml(obj, {
    name: config.name
  , level: config.level
  , arrayRoot: config.arrayRoot
  });

  if (!config.whitespace) {
    xml = xml.replace(/>\n/g, '>');
  }

  return xml;
}
```
- example usage
```shell
...
  version = arr.join('.');

  // Update package.json or other files with the new version-info
  self.versionFiles.forEach(function (file) {
    var p = path.join(process.cwd(), file)
      , data = JSON.parse(fs.readFileSync(p).toString());
    data.version = version;
    fs.writeFileSync(p, JSON.stringify(data, true, 2) + '\n');
  });
  // Return the version string so that listeners for the 'complete' event
  // for this task can use it (e.g., to update other files before pushing
  // to Git)
  return version;
});
...
```



# <a name="apidoc.module.jake.api"></a>[module jake.api](#apidoc.module.jake.api)

#### <a name="apidoc.element.jake.api.complete"></a>[function <span class="apidocSignatureSpan">jake.api.</span>complete (task, val)](#apidoc.element.jake.api.complete)
- description and source-code
```javascript
complete = function (task, val) {
  //this should detect if the first arg is a task, but I guess it should be more thorough
  if(task && task. _currentPrereqIndex >=0 ) {
    task.complete(val);
  } else {
    val = task;
    if(jake._invocationChain.length > 0) {
      jake._invocationChain[jake._invocationChain.length-1].complete(val);
    } else {
    }
  }
}
```
- example usage
```shell
...
@static
@function
@description Completes an asynchronous task, allowing Jake's
execution to proceed to the next task. Calling complete globally or without
arguments completes the last task on the invocationChain. If you use parallel
execution of prereqs this will probably complete a wrong task. You should call this
function with this task as the first argument, before the optional return value.
Alternatively you can call task.complete()
'
@example
task('generate', ['doc:clobber'], function () {
  exec('./generate_docs.sh', function (err, stdout, stderr) {
    if (err || stderr) {
      fail(err || stderr);
    }
...
```

#### <a name="apidoc.element.jake.api.desc"></a>[function <span class="apidocSignatureSpan">jake.api.</span>desc (description)](#apidoc.element.jake.api.desc)
- description and source-code
```javascript
desc = function (description) {
  jake.currentTaskDescription = description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.directory"></a>[function <span class="apidocSignatureSpan">jake.api.</span>directory (name)](#apidoc.element.jake.api.directory)
- description and source-code
```javascript
directory = function (name) {
  var args = Array.prototype.slice.call(arguments)
    , createdTask;
  args.unshift('directory');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.fail"></a>[function <span class="apidocSignatureSpan">jake.api.</span>fail (err, code)](#apidoc.element.jake.api.fail)
- description and source-code
```javascript
fail = function (err, code) {
  var msg
    , errObj;
  if (code) {
    jake.errorCode = code;
  }
  if (err) {
    if (typeof err == 'string') {
      // Use the initial or only line of the error as the error-message
      // If there was a multi-line error, use the rest as the stack
      msg = err.split('\n');
      errObj = new Error(msg.shift());
      if (msg.length) {
        errObj.stack = msg.join('\n');
      }
      throw errObj;
    }
    else if (err instanceof Error) {
      throw err;
    }
    else {
      throw new Error(err.toString());
    }
  }
  else {
    throw new Error();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.file"></a>[function <span class="apidocSignatureSpan">jake.api.</span>file (name, prereqs, action, opts)](#apidoc.element.jake.api.file)
- description and source-code
```javascript
file = function (name, prereqs, action, opts) {
  var args = Array.prototype.slice.call(arguments)
    , createdTask;
  args.unshift('file');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.namespace"></a>[function <span class="apidocSignatureSpan">jake.api.</span>namespace (name, closure)](#apidoc.element.jake.api.namespace)
- description and source-code
```javascript
namespace = function (name, closure) {
  var curr = jake.currentNamespace
    , ns = curr.childNamespaces[name] || new jake.Namespace(name, curr);
  curr.childNamespaces[name] = ns;
  jake.currentNamespace = ns;
  closure();
  jake.currentNamespace = curr;
  jake.currentTaskDescription = null;
  return ns;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.npmPublishTask"></a>[function <span class="apidocSignatureSpan">jake.api.</span>npmPublishTask (name, prereqs, opts, definition)](#apidoc.element.jake.api.npmPublishTask)
- description and source-code
```javascript
npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.packageTask"></a>[function <span class="apidocSignatureSpan">jake.api.</span>packageTask (name, version, definition)](#apidoc.element.jake.api.packageTask)
- description and source-code
```javascript
packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.publishTask"></a>[function <span class="apidocSignatureSpan">jake.api.</span>publishTask (name, prereqs, opts, definition)](#apidoc.element.jake.api.publishTask)
- description and source-code
```javascript
publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.rule"></a>[function <span class="apidocSignatureSpan">jake.api.</span>rule ()](#apidoc.element.jake.api.rule)
- description and source-code
```javascript
rule = function () {
  var args = Array.prototype.slice.call(arguments)
    , arg
    , pattern = args.shift()
    , source = args.shift()
    , prereqs = []
    , action = function () {}
    , opts = {}
    , key = pattern.toString(); // May be a RegExp

  while ((arg = args.shift())) {
    if (typeof arg == 'function') {
      action = arg;
    }
    else if (Array.isArray(arg)) {
      prereqs = arg;
    }
    else {
      opts = arg;
    }
  }

  jake.currentNamespace.rules[key] = new jake.Rule({
    pattern: pattern
  , source: source
  , prereqs: prereqs
  , action: action
  , opts: opts
  , desc: jake.currentTaskDescription
  , ns: jake.currentNamespace
  });
  jake.currentTaskDescription = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.task"></a>[function <span class="apidocSignatureSpan">jake.api.</span>task (name, prereqs, action, opts)](#apidoc.element.jake.api.task)
- description and source-code
```javascript
task = function (name, prereqs, action, opts) {
  var args = Array.prototype.slice.call(arguments)
    , type
    , createdTask;
  args.unshift('task');
  createdTask = jake.createTask.apply(global, args);
  jake.currentTaskDescription = null;
  return createdTask;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.testTask"></a>[function <span class="apidocSignatureSpan">jake.api.</span>testTask ()](#apidoc.element.jake.api.testTask)
- description and source-code
```javascript
testTask = function () {
  var ctor = function () {}
    , t;
  ctor.prototype = jake.TestTask.prototype;
  t = new ctor();
  jake.TestTask.apply(t, arguments);
  return t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.api.watchTask"></a>[function <span class="apidocSignatureSpan">jake.api.</span>watchTask (name, taskNames, definition)](#apidoc.element.jake.api.watchTask)
- description and source-code
```javascript
watchTask = function (name, taskNames, definition) {
  return new jake.WatchTask(name, taskNames, definition);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.array"></a>[module jake.array](#apidoc.module.jake.array)

#### <a name="apidoc.element.jake.array.humanize"></a>[function <span class="apidocSignatureSpan">jake.array.</span>humanize (a)](#apidoc.element.jake.array.humanize)
- description and source-code
```javascript
humanize = function (a) {
  var array = a.slice();
  // If array only has one item then just return it
  if (array.length <= 1) {
    return String(array);
  }

  var last = array.pop()
    , items = array.join(', ');

  return items + ' and ' + last;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.array.include"></a>[function <span class="apidocSignatureSpan">jake.array.</span>include (array, item)](#apidoc.element.jake.array.include)
- description and source-code
```javascript
include = function (array, item) {
  var res = -1;
  if (typeof array.indexOf == 'function') {
    res = array.indexOf(item);
  }
  else {
    for (var i = 0, ii = array.length; i < ii; i++) {
      if (array[i] == item) {
        res = i;
        break;
      }
    }
  }
  return res > -1;
}
```
- example usage
```shell
...
  , 'package.json'
  , 'app/*'
  , 'bin/*'
  , 'config/*'
  , 'lib/*'
  , 'node_modules/*'
  ];
  this.packageFiles.include(files);
  this.packageFiles.exclude('node_modules/foobar');
  this.needTarGz = true;
});

 */
var PackageTask = function () {
var args = Array.prototype.slice.call(arguments)
...
```

#### <a name="apidoc.element.jake.array.included"></a>[function <span class="apidocSignatureSpan">jake.array.</span>included (item, array)](#apidoc.element.jake.array.included)
- description and source-code
```javascript
included = function (item, array) {
  var result = array.indexOf(item);

  if (result === -1) {
    return false;
  } else {
    return array;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async"></a>[module jake.async](#apidoc.module.jake.async)

#### <a name="apidoc.element.jake.async.AsyncCall"></a>[function <span class="apidocSignatureSpan">jake.async.</span>AsyncCall (func, args, callback, context)](#apidoc.element.jake.async.AsyncCall)
- description and source-code
```javascript
AsyncCall = function (func, args, callback, context) {
  this.func = func;
  this.args = args;
  this.callback = callback || null;
  this.context = context || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain"></a>[function <span class="apidocSignatureSpan">jake.async.</span>AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain)
- description and source-code
```javascript
AsyncChain = function (chain) {
  this.init(chain);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncGroup"></a>[function <span class="apidocSignatureSpan">jake.async.</span>AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup)
- description and source-code
```javascript
AsyncGroup = function (group) {
  var item;
  var callback;
  var args;

  this.group = [];
  this.outstandingCount = 0;

  for (var i = 0; i < group.length; i++) {
    item = group[i];
    this.group.push(new async.AsyncCall(
        item.func, item.args, item.callback, item.context));
    this.outstandingCount++;
  }

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.Initializer"></a>[function <span class="apidocSignatureSpan">jake.async.</span>Initializer (steps, callback)](#apidoc.element.jake.async.Initializer)
- description and source-code
```javascript
Initializer = function (steps, callback) {
  var self = this;
  this.steps = {};
  this.callback = callback;
  // Create an object-literal of the steps to tick off
  steps.forEach(function (step) {
    self.steps[step] = false;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.SimpleAsyncChain"></a>[function <span class="apidocSignatureSpan">jake.async.</span>SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain)
- description and source-code
```javascript
SimpleAsyncChain = function (funcs, context) {
  var chain = [];
  for (var i = 0, ii = funcs.length; i < ii; i++) {
    chain.push(_createSimpleAsyncCall(funcs[i], context));
  }
  this.init(chain);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.execNonBlocking"></a>[function <span class="apidocSignatureSpan">jake.async.</span>execNonBlocking (func)](#apidoc.element.jake.async.execNonBlocking)
- description and source-code
```javascript
execNonBlocking = function (func) {
  if (typeof process != 'undefined' && typeof process.nextTick == 'function') {
    process.nextTick(func);
  }
  else {
    setTimeout(func, 0);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.AsyncChain"></a>[module jake.async.AsyncChain](#apidoc.module.jake.async.AsyncChain)

#### <a name="apidoc.element.jake.async.AsyncChain.AsyncChain"></a>[function <span class="apidocSignatureSpan">jake.async.</span>AsyncChain (chain)](#apidoc.element.jake.async.AsyncChain.AsyncChain)
- description and source-code
```javascript
AsyncChain = function (chain) {
  this.init(chain);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.AsyncChain.prototype"></a>[module jake.async.AsyncChain.prototype](#apidoc.module.jake.async.AsyncChain.prototype)

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.abort"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>abort ()](#apidoc.element.jake.async.AsyncChain.prototype.abort)
- description and source-code
```javascript
abort = function () {
  this.aborted = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.addItem"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>addItem (item)](#apidoc.element.jake.async.AsyncChain.prototype.addItem)
- description and source-code
```javascript
addItem = function (item) {
  this.chain.push(new async.AsyncCall(
    item.func, item.args || [], item.callback, item.context));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.execCallback"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>execCallback ()](#apidoc.element.jake.async.AsyncChain.prototype.execCallback)
- description and source-code
```javascript
execCallback = function () {
  // Look up the callback, if any, specified for this async call
  var callback = this.currentItem.callback;
  // If there's a callback, do it
  if (callback && typeof callback == 'function') {
    // Allow access to the chain from inside the callback by setting
    // callback.chain = this, and then using arguments.callee.chain
    callback.chain = this;
    callback.apply(this.currentItem.context, arguments);
  }

  this.currentItem.finished = true;

  // If one of the async callbacks called chain.shortCircuit,
  // skip to the 'last' function for the chain
  if (this.shortCircuited) {
    this.last.apply(null, this.shortCircuitedArgs);
  }
  // If one of the async callbacks called chain.abort,
  // bail completely out
  else if (this.aborted) {
    return;
  }
  // Otherwise run the next item, if any, in the chain
  // Let's try not to block if we don't have to
  else {
    // Scopage
    var _this = this;
    async.execNonBlocking(function () { _this.next.call(_this); });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.init"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>init (chain)](#apidoc.element.jake.async.AsyncChain.prototype.init)
- description and source-code
```javascript
init = function (chain) {
  var item;
  this.chain = [];
  this.currentItem = null;
  this.shortCircuited = false;
  this.shortCircuitedArgs = undefined;
  this.aborted = false;

  for (var i = 0; i < chain.length; i++) {
    item = chain[i];
    this.addItem(item);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.last"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>last ()](#apidoc.element.jake.async.AsyncChain.prototype.last)
- description and source-code
```javascript
last = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.next"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>next ()](#apidoc.element.jake.async.AsyncChain.prototype.next)
- description and source-code
```javascript
next = function () {
  if (this.chain.length) {
    this.runItem(this.chain.shift());
  }
  else {
    this.last();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.push"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>push (item)](#apidoc.element.jake.async.AsyncChain.prototype.push)
- description and source-code
```javascript
push = function (item) {
  this.chain.push(new async.AsyncCall(
    item.func, item.args || [], item.callback, item.context));
}
```
- example usage
```shell
...
        this.parentNamespace.matchRule(relativeName));
  };

  this.getPath = function () {
    var parts = []
      , next = this;
    while (!!next) {
      parts.push(next.name);
      next = next.parentNamespace;
    }
    parts.pop(); // Remove 'default'
    return parts.reverse().join(':');
  };

})();
...
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.run"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>run ()](#apidoc.element.jake.async.AsyncChain.prototype.run)
- description and source-code
```javascript
run = function () {
  if (this.chain.length) {
    this.runItem(this.chain.shift());
  }
  else {
    this.last();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.runItem"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>runItem (item)](#apidoc.element.jake.async.AsyncChain.prototype.runItem)
- description and source-code
```javascript
runItem = function (item) {
  // Reference to the current item in the chain -- used
  // to look up the callback to execute with execCallback
  this.currentItem = item;
  // Scopage
  var _this = this;
  // Pass the arguments passed to the current async call
  // to the callback executor, execute it in the correct scope
  var executor = function () {
    _this.execCallback.apply(_this, arguments);
  };
  // Append the callback executor to the end of the arguments
  // Node helpfully always has the callback func last
  var args = item.args.concat(executor);
  var func = item.func;
  // Run the async call
  func.apply(item.context, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncChain.prototype.shortCircuit"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncChain.prototype.</span>shortCircuit ()](#apidoc.element.jake.async.AsyncChain.prototype.shortCircuit)
- description and source-code
```javascript
shortCircuit = function () {
  this.shortCircuitedArgs = arguments;
  this.shortCircuited = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.AsyncGroup"></a>[module jake.async.AsyncGroup](#apidoc.module.jake.async.AsyncGroup)

#### <a name="apidoc.element.jake.async.AsyncGroup.AsyncGroup"></a>[function <span class="apidocSignatureSpan">jake.async.</span>AsyncGroup (group)](#apidoc.element.jake.async.AsyncGroup.AsyncGroup)
- description and source-code
```javascript
AsyncGroup = function (group) {
  var item;
  var callback;
  var args;

  this.group = [];
  this.outstandingCount = 0;

  for (var i = 0; i < group.length; i++) {
    item = group[i];
    this.group.push(new async.AsyncCall(
        item.func, item.args, item.callback, item.context));
    this.outstandingCount++;
  }

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.AsyncGroup.prototype"></a>[module jake.async.AsyncGroup.prototype](#apidoc.module.jake.async.AsyncGroup.prototype)

#### <a name="apidoc.element.jake.async.AsyncGroup.prototype.finish"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>finish ()](#apidoc.element.jake.async.AsyncGroup.prototype.finish)
- description and source-code
```javascript
finish = function () {
  this.outstandingCount--;
  if (!this.outstandingCount) {
    this.last();
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncGroup.prototype.last"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>last ()](#apidoc.element.jake.async.AsyncGroup.prototype.last)
- description and source-code
```javascript
last = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.async.AsyncGroup.prototype.run"></a>[function <span class="apidocSignatureSpan">jake.async.AsyncGroup.prototype.</span>run ()](#apidoc.element.jake.async.AsyncGroup.prototype.run)
- description and source-code
```javascript
run = function () {
  var _this = this
    , group = this.group
    , item
    , createItem = function (item, args) {
        return function () {
          item.func.apply(item.context, args);
        };
      }
    , createCallback = function (item) {
        return function () {
          if (item.callback) {
            item.callback.apply(null, arguments);
          }
          _this.finish.call(_this);
        }
      };

  for (var i = 0; i < group.length; i++) {
    item = group[i];
    callback = createCallback(item);
    args = item.args.concat(callback);
    // Run the async call
    async.execNonBlocking(createItem(item, args));
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.Initializer"></a>[module jake.async.Initializer](#apidoc.module.jake.async.Initializer)

#### <a name="apidoc.element.jake.async.Initializer.Initializer"></a>[function <span class="apidocSignatureSpan">jake.async.</span>Initializer (steps, callback)](#apidoc.element.jake.async.Initializer.Initializer)
- description and source-code
```javascript
Initializer = function (steps, callback) {
  var self = this;
  this.steps = {};
  this.callback = callback;
  // Create an object-literal of the steps to tick off
  steps.forEach(function (step) {
    self.steps[step] = false;
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.async.Initializer.prototype"></a>[module jake.async.Initializer.prototype](#apidoc.module.jake.async.Initializer.prototype)

#### <a name="apidoc.element.jake.async.Initializer.prototype.complete"></a>[function <span class="apidocSignatureSpan">jake.async.Initializer.prototype.</span>complete (step)](#apidoc.element.jake.async.Initializer.prototype.complete)
- description and source-code
```javascript
complete = function (step) {
  var steps = this.steps;
  // Tick this step off
  steps[step] = true;
  // Iterate the steps -- if any are not done, bail out
  for (var p in steps) {
    if (!steps[p]) {
      return false;
    }
  }
  // If all steps are done, run the callback
  this.callback();
}
```
- example usage
```shell
...
@static
@function
@description Completes an asynchronous task, allowing Jake's
execution to proceed to the next task. Calling complete globally or without
arguments completes the last task on the invocationChain. If you use parallel
execution of prereqs this will probably complete a wrong task. You should call this
function with this task as the first argument, before the optional return value.
Alternatively you can call task.complete()
'
@example
task('generate', ['doc:clobber'], function () {
  exec('./generate_docs.sh', function (err, stdout, stderr) {
    if (err || stderr) {
      fail(err || stderr);
    }
...
```



# <a name="apidoc.module.jake.async.SimpleAsyncChain"></a>[module jake.async.SimpleAsyncChain](#apidoc.module.jake.async.SimpleAsyncChain)

#### <a name="apidoc.element.jake.async.SimpleAsyncChain.SimpleAsyncChain"></a>[function <span class="apidocSignatureSpan">jake.async.</span>SimpleAsyncChain (funcs, context)](#apidoc.element.jake.async.SimpleAsyncChain.SimpleAsyncChain)
- description and source-code
```javascript
SimpleAsyncChain = function (funcs, context) {
  var chain = [];
  for (var i = 0, ii = funcs.length; i < ii; i++) {
    chain.push(_createSimpleAsyncCall(funcs[i], context));
  }
  this.init(chain);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.date"></a>[module jake.date](#apidoc.module.jake.date)

#### <a name="apidoc.element.jake.date.add"></a>[function <span class="apidocSignatureSpan">jake.date.</span>add (dt, interv, incr)](#apidoc.element.jake.date.add)
- description and source-code
```javascript
add = function (dt, interv, incr) {
  if (typeof dt == 'number') { dt = new Date(dt); }
  function fixOvershoot() {
    if (sum.getDate() < dt.getDate()) {
      sum.setDate(0);
    }
  }
  var key = datePartsMap[interv];
  var sum = new Date(dt);
  switch (key) {
    case dateParts.YEAR:
      sum.setFullYear(dt.getFullYear()+incr);
      // Keep increment/decrement from 2/29 out of March
      fixOvershoot();
      break;
    case dateParts.QUARTER:
      // Naive quarter is just three months
      incr*=3;
      // fallthrough...
    case dateParts.MONTH:
      sum.setMonth(dt.getMonth()+incr);
      // Reset to last day of month if you overshoot
      fixOvershoot();
      break;
    case dateParts.WEEK:
      incr*=7;
      // fallthrough...
    case dateParts.DAY:
      sum.setDate(dt.getDate() + incr);
      break;
    case dateParts.WEEKDAY:
      //FIXME: assumes Saturday/Sunday weekend, but even this is not fixed.
      // There are CLDR entries to localize this.
      var dat = dt.getDate();
      var weeks = 0;
      var days = 0;
      var strt = 0;
      var trgt = 0;
      var adj = 0;
      // Divide the increment time span into weekspans plus leftover days
      // e.g., 8 days is one 5-day weekspan / and two leftover days
      // Can't have zero leftover days, so numbers divisible by 5 get
      // a days value of 5, and the remaining days make up the number of weeks
      var mod = incr % 5;
      if (mod == 0) {
        days = (incr > 0) ? 5 : -5;
        weeks = (incr > 0) ? ((incr-5)/5) : ((incr+5)/5);
      }
      else {
        days = mod;
        weeks = parseInt(incr/5);
      }
      // Get weekday value for orig date param
      strt = dt.getDay();
      // Orig date is Sat / positive incrementer
      // Jump over Sun
      if (strt == 6 && incr > 0) {
        adj = 1;
      }
      // Orig date is Sun / negative incrementer
      // Jump back over Sat
      else if (strt == 0 && incr < 0) {
        adj = -1;
      }
      // Get weekday val for the new date
      trgt = strt + days;
      // New date is on Sat or Sun
      if (trgt == 0 || trgt == 6) {
        adj = (incr > 0) ? 2 : -2;
      }
      // Increment by number of weeks plus leftover days plus
      // weekend adjustments
      sum.setDate(dat + (7*weeks) + days + adj);
      break;
    case dateParts.HOUR:
      sum.setHours(sum.getHours()+incr);
      break;
    case dateParts.MINUTE:
      sum.setMinutes(sum.getMinutes()+incr);
      break;
    case dateParts.SECOND:
      sum.setSeconds(sum.getSeconds()+incr);
      break;
    case dateParts.MILLISECOND:
      sum.setMilliseconds(sum.getMilliseconds()+incr);
      break;
    default:
      // Do nothing
      break;
  }
  return sum; // Date
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.calcCentury"></a>[function <span class="apidocSignatureSpan">jake.date.</span>calcCentury (year)](#apidoc.element.jake.date.calcCentury)
- description and source-code
```javascript
calcCentury = function (year) {
  if(!year) {
    year = _date.getFullYear();
  }

  var ret = parseInt((year / 100) + 1);
  year = year.toString();

  // If year ends in 00 subtract one, because it's still the century before the one
  // it divides to
  if (year.substring(year.length - 2) === '00') {
    ret--;
  }

  return ret.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.calcDays"></a>[function <span class="apidocSignatureSpan">jake.date.</span>calcDays (dt)](#apidoc.element.jake.date.calcDays)
- description and source-code
```javascript
calcDays = function (dt) {
  var first = new Date(dt.getFullYear(), 0, 1);
  var diff = 0;
  var ret = 0;
  first = first.getTime();
  diff = (dt.getTime() - first);
  ret = parseInt(((((diff/1000)/60)/60)/24))+1;
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.convertOneBase"></a>[function <span class="apidocSignatureSpan">jake.date.</span>convertOneBase (d)](#apidoc.element.jake.date.convertOneBase)
- description and source-code
```javascript
convertOneBase = function (d) {
  return d == 0 ? 7 : d;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.diff"></a>[function <span class="apidocSignatureSpan">jake.date.</span>diff (date1, date2, interv)](#apidoc.element.jake.date.diff)
- description and source-code
```javascript
diff = function (date1, date2, interv) {
  //  date1
  //    Date object or Number equivalent
  //
  //  date2
  //    Date object or Number equivalent
  //
  //  interval
  //    A constant representing the interval, e.g. YEAR, MONTH, DAY.  See this.dateParts.

  // Accept timestamp input
  if (typeof date1 == 'number') { date1 = new Date(date1); }
  if (typeof date2 == 'number') { date2 = new Date(date2); }
  var yeaDiff = date2.getFullYear() - date1.getFullYear();
  var monDiff = (date2.getMonth() - date1.getMonth()) + (yeaDiff * 12);
  var msDiff = date2.getTime() - date1.getTime(); // Millisecs
  var secDiff = msDiff/1000;
  var minDiff = secDiff/60;
  var houDiff = minDiff/60;
  var dayDiff = houDiff/24;
  var weeDiff = dayDiff/7;
  var delta = 0; // Integer return value

  var key = datePartsMap[interv];
  switch (key) {
    case dateParts.YEAR:
      delta = yeaDiff;
      break;
    case dateParts.QUARTER:
      var m1 = date1.getMonth();
      var m2 = date2.getMonth();
      // Figure out which quarter the months are in
      var q1 = Math.floor(m1/3) + 1;
      var q2 = Math.floor(m2/3) + 1;
      // Add quarters for any year difference between the dates
      q2 += (yeaDiff * 4);
      delta = q2 - q1;
      break;
    case dateParts.MONTH:
      delta = monDiff;
      break;
    case dateParts.WEEK:
      // Truncate instead of rounding
      // Don't use Math.floor -- value may be negative
      delta = parseInt(weeDiff);
      break;
    case dateParts.DAY:
      delta = dayDiff;
      break;
    case dateParts.WEEKDAY:
      var days = Math.round(dayDiff);
      var weeks = parseInt(days/7);
      var mod = days % 7;

      // Even number of weeks
      if (mod == 0) {
        days = weeks*5;
      }
      else {
        // Weeks plus spare change (< 7 days)
        var adj = 0;
        var aDay = date1.getDay();
        var bDay = date2.getDay();

        weeks = parseInt(days/7);
        mod = days % 7;
        // Mark the date advanced by the number of
        // round weeks (may be zero)
        var dtMark = new Date(date1);
        dtMark.setDate(dtMark.getDate()+(weeks*7));
        var dayMark = dtMark.getDay();

        // Spare change days -- 6 or less
        if (dayDiff > 0) {
          switch (true) {
            // Range starts on Sat
            case aDay == 6:
              adj = -1;
              break;
            // Range starts on Sun
            case aDay == 0:
              adj = 0;
              break;
            // Range ends on Sat
            case bDay == 6:
              adj = -1;
              break;
            // Range ends on Sun
            case bDay == 0:
              adj = -2;
              break;
            // Range contains weekend
            case (dayMark + mod) > 5:
              adj = -2;
              break;
            default:
              // Do nothing
              break;
          }
        }
        else if (dayDiff < 0) {
          switch (true) {
            // Range starts on Sat
            case aDay == 6:
              adj = 0;
              break;
            // Range starts on Sun
            case aDay == 0:
              adj = 1;
              break;
            // Range ends on Sat
            case bDay == 6:
              adj = 2;
              break;
            // Range ends on Sun
            case bDay == 0:
              adj = 1;
              break;
            // Range contains weekend
            case (dayMark + mod) < 0:
              adj = 2;
              break;
            default:
              // Do nothing
              break;
          }
        }
        days += adj;
        days -= (weeks*2);
      }
      delta = days;

      break;
    case dateParts.HOUR:
      delta = houDiff;
      break;
    case dateParts.MINUTE:
      delta = minDiff;
      break;
    case dateParts.SECOND:
      delta = secDiff;
      break;
    case dateParts.MILLISECOND:
      delta = msDiff;
      break;
    default:
      // Do nothing
      break;
  }
  // Round for fractional values and DST leaps
  return Math.round(delta); // Number (integer)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.getMeridian"></a>[function <span class="apidocSignatureSpan">jake.date.</span>getMeridian (h)](#apidoc.element.jake.date.getMeridian)
- description and source-code
```javascript
getMeridian = function (h) {
  return h > 11 ? this.meridiem.PM :
    this.meridiem.AM;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.getMeridiem"></a>[function <span class="apidocSignatureSpan">jake.date.</span>getMeridiem (h)](#apidoc.element.jake.date.getMeridiem)
- description and source-code
```javascript
getMeridiem = function (h) {
  return h > 11 ? this.meridiem.PM :
    this.meridiem.AM;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.getSupportedFormats"></a>[function <span class="apidocSignatureSpan">jake.date.</span>getSupportedFormats ()](#apidoc.element.jake.date.getSupportedFormats)
- description and source-code
```javascript
getSupportedFormats = function () {
  var str = '';
  for (var i in this.supportedFormats) { str += i; }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.getTwoDigitYear"></a>[function <span class="apidocSignatureSpan">jake.date.</span>getTwoDigitYear (yr)](#apidoc.element.jake.date.getTwoDigitYear)
- description and source-code
```javascript
getTwoDigitYear = function (yr) {
  // Add a millenium to take care of years before the year 1000,
  // (e.g, the year 7) since we're only taking the last two digits
  // If we overshoot, it doesn't matter
  var millenYear = yr + 1000;
  var str = millenYear.toString();
  str = str.substr(2); // Get the last two digits
  return str
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.hrMil2Std"></a>[function <span class="apidocSignatureSpan">jake.date.</span>hrMil2Std (hour)](#apidoc.element.jake.date.hrMil2Std)
- description and source-code
```javascript
hrMil2Std = function (hour) {
  var h = typeof hour == 'number' ? hour : parseInt(hour);
  var str = h > 12 ? h - 12 : h;
  str = str == 0 ? 12 : str;
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.hrStd2Mil"></a>[function <span class="apidocSignatureSpan">jake.date.</span>hrStd2Mil (hour, pm)](#apidoc.element.jake.date.hrStd2Mil)
- description and source-code
```javascript
hrStd2Mil = function (hour, pm) {
  var h = typeof hour == 'number' ? hour : parseInt(hour);
  var str = '';
  // PM
  if (pm) {
    str = h < 12 ? (h+12) : h;
  }
  // AM
  else {
    str = h == 12 ? 0 : h;
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.parse"></a>[function <span class="apidocSignatureSpan">jake.date.</span>parse (val, options)](#apidoc.element.jake.date.parse)
- description and source-code
```javascript
parse = function (val, options) {
  var dt
    , opts = options || {}
    , matches
    , reordered
    , off
    , posOff
    , offHours
    , offMinutes
    , offSeconds
    , curr
    , stamp
    , utc;

  // Yay, we have a date, use it as-is
  if (val instanceof Date || typeof val.getFullYear == 'function') {
    dt = val;
  }

  // Timestamp?
  else if (typeof val == 'number') {
    dt = new Date(val);
  }

  // String or Array
  else {
    // Value preparsed, looks like [yyyy, mo, dd, hh, mi, ss, ms, (offset?)]
    if (_isArray(val)) {
      matches = val;
      matches.unshift(null);
      matches[8] = null;
    }

    // Oh, crap, it's a string -- parse this bitch
    else if (typeof val == 'string') {
      matches = val.match(_DATETIME_PAT);

      // Stupid US-only format?
      if (!matches) {
        matches = val.match(_US_DATE_PAT);
        if (matches) {
          reordered = [matches[0], matches[3], matches[1], matches[2]];
          // Pad the results to the same length as ISO8601
          reordered[8] = null;
          matches = reordered;
        }
      }

      // Time-stored-in-Date hack?
      if (!matches) {
        matches = val.match(_TIME_PAT);
        if (matches) {
          reordered = [matches[0], 0, 1, 0, matches[1],
              matches[2], matches[3], matches[4], null];
          matches = reordered;
        }
      }

    }

    // Sweet, the regex actually parsed it into something useful
    if (matches) {
      matches.shift(); // First match is entire match, DO NOT WANT

      off = matches.pop();
      // If there's an offset (or the 'Z' non-offset offset), use UTC
      // methods to set everything
      if (off) {
        if (off == 'Z') {
          utc = true;
          offSeconds = 0;
        }
        else {
          utc = false;
          // Convert from extended to basic if necessary
          off = off.replace(/:/g, '');
          // '+0000' will still be zero
          if (parseInt(off, 10) === 0) {
            utc = true;
          }
          else {
            posOff = off.indexOf('+') === 0;
            // Strip plus or minus
            off = off.substr(1);

            offHours = parseInt(off.substr(0, 2), 10);

            offMinutes = off.substr(2, 2);
            if (offMinutes) {
              offMinutes = parseInt(offMinutes, 10);
            }
            else {
              offMinutes = 0;
            }

            offSeconds = off.substr(4, 2);
            if (offSeconds) {
              offSeconds = parseInt(offSeconds, 10);
            }
            else {
              offSeconds = 0;
            }

            offSeconds += (offMinutes * 60)
            offSeconds += (offHours * 60 * 60);
            if (!posOff) {
              offSeconds = 0 - offSeconds;
            }
          }
        }
      }

      dt = new Date(0);

      // Stupid zero-based months
      matches[1] = parseInt(matches[1], 10) - 1;

      // Specific offset, iterate the array and set each date property
      // using UTC setters, then adjust time using offset
      if (off) {
        for (var i = matches.length - 1; i > -1; i--) {
          curr = parseInt(matches[i], 10) || 0;
          dt['setUTC' + _dateMethods[i]](curr);
        }
        // Add any offset
        dt.setSeconds(dt.getSeconds() - offSeconds);
      }
      // Otherwise we know nothing about the offset, just iterate the
      // array and set each date property using regular setters
      else {
        var lastValIndex;
        for (var i = matches.length - 1; i > -1; i--) {
          if (matches[i]) {
            curr = parseInt(matches[i], 10);
            if (typeof lastValIndex == 'undefined') {
              lastValIndex = i;
            }
          }
          else {
            curr = 0;
          }
          dt['set' + _dateMethods[i]](curr);
        }
        if (opts.setMax) {
          for (var i = lastValIndex + 1, ii = matches.length; i < ii; i++) {
            switch (i) {
              case 3:
                dt['set' + _dateMethods[i]](23);
                break;
              case 4: ...
```
- example usage
```shell
...
      jake.errorCode = jake.errorCode || 1;
      process.exit(jake.errorCode);
    });
  });
};

this.parseArgs = function (args) {
  var result = (new parseargs.Parser(optsReg)).parse(args);
  this.setOpts(result.opts);
  this.setTaskNames(result.taskNames);
  this.setEnvVars(result.envVars);
};

this.setOpts = function (options) {
  var opts = options || {};
...
```

#### <a name="apidoc.element.jake.date.relativeTime"></a>[function <span class="apidocSignatureSpan">jake.date.</span>relativeTime (dt, options)](#apidoc.element.jake.date.relativeTime)
- description and source-code
```javascript
relativeTime = function (dt, options) {
  var opts = options || {}
    , now = opts.now || new Date()
    , abbr = opts.abbreviated || false
    , format = opts.format || '%F %T'
  // Diff in seconds
    , diff = (now.getTime() - dt.getTime()) / 1000
    , ret
    , num
    , hour = 60*60
    , day = 24*hour
    , week = 7*day
    , month = 30*day;
  switch (true) {
    case diff < 60:
      ret = abbr ? '<1m' : 'less than a minute ago';
      break;
    case diff < 120:
      ret = abbr ? '1m' : 'about a minute ago';
      break;
    case diff < (45*60):
      num = parseInt((diff / 60), 10);
      ret = abbr ? num + 'm' : num + ' minutes ago';
      break;
    case diff < (2*hour):
      ret = abbr ? '1h' : 'about an hour ago';
      break;
    case diff < (1*day):
      num = parseInt((diff / hour), 10);
      ret = abbr ? num + 'h' : 'about ' + num + ' hours ago';
      break;
    case diff < (2*day):
      ret = abbr ? '1d' : 'one day ago';
      break;
    case diff < (7*day):
      num = parseInt((diff / day), 10);
      ret = abbr ? num + 'd' : 'about ' + num + ' days ago';
      break;
    case diff < (11*day):
      ret = abbr ? '1w': 'one week ago';
      break;
    case diff < (1*month):
      num = Math.round(diff / week);
      ret = abbr ? num + 'w' : 'about ' + num + ' weeks ago';
      break;
    default:
      ret = date.strftime(dt, format);
      break;
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.strftime"></a>[function <span class="apidocSignatureSpan">jake.date.</span>strftime (dt, format)](#apidoc.element.jake.date.strftime)
- description and source-code
```javascript
strftime = function (dt, format) {
  if (!dt) { return '' }

  var d = dt;
  var pats = [];
  var dts = [];
  var str = format;
  var key;

  // Allow either Date obj or UTC stamp
  d = typeof dt == 'number' ? new Date(dt) : dt;

  // Grab all instances of expected formats into array
  while (pats = this.supportedFormatsPat.exec(format)) {
    dts.push(pats[0]);
  }

  // Process any hits
  for (var i = 0; i < dts.length; i++) {
    key = dts[i].replace(/%/, '');
    str = str.replace('%' + key,
      this.supportedFormats[key](d));
  }
  return str;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.strftimeNotImplemented"></a>[function <span class="apidocSignatureSpan">jake.date.</span>strftimeNotImplemented (s)](#apidoc.element.jake.date.strftimeNotImplemented)
- description and source-code
```javascript
strftimeNotImplemented = function (s) {
  throw('this.strftime format "' + s + '" not implemented.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.toISO8601"></a>[function <span class="apidocSignatureSpan">jake.date.</span>toISO8601 (dt, options)](#apidoc.element.jake.date.toISO8601)
- description and source-code
```javascript
toISO8601 = function (dt, options) {
  var opts = options || {}
    , off = dt.getTimezoneOffset()
    , offHours
    , offMinutes
    , str = this.strftime(dt, '%F') + 'T'
        + this.strftime(dt, '%T') + '.'
        + string.lpad(dt.getMilliseconds(), '0', 3);

  if (opts.tz) {
    // Pos and neg numbers are both truthy; only
    // zero is falsy
    if (off && !opts.utc) {
      str += off > 0 ? '-' : '+';
      offHours = parseInt(off / 60, 10);
      str += string.lpad(offHours, '0', 2);
      offMinutes = off % 60;
      if (offMinutes) {
        str += string.lpad(offMinutes, '0', 2);
      }
    }
    else {
      str += 'Z';
    }
  }

  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.toIso8601"></a>[function <span class="apidocSignatureSpan">jake.date.</span>toIso8601 (dt, options)](#apidoc.element.jake.date.toIso8601)
- description and source-code
```javascript
toIso8601 = function (dt, options) {
  var opts = options || {}
    , off = dt.getTimezoneOffset()
    , offHours
    , offMinutes
    , str = this.strftime(dt, '%F') + 'T'
        + this.strftime(dt, '%T') + '.'
        + string.lpad(dt.getMilliseconds(), '0', 3);

  if (opts.tz) {
    // Pos and neg numbers are both truthy; only
    // zero is falsy
    if (off && !opts.utc) {
      str += off > 0 ? '-' : '+';
      offHours = parseInt(off / 60, 10);
      str += string.lpad(offHours, '0', 2);
      offMinutes = off % 60;
      if (offMinutes) {
        str += string.lpad(offMinutes, '0', 2);
      }
    }
    else {
      str += 'Z';
    }
  }

  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.toUTC"></a>[function <span class="apidocSignatureSpan">jake.date.</span>toUTC (dt)](#apidoc.element.jake.date.toUTC)
- description and source-code
```javascript
toUTC = function (dt) {
  return new Date(
      dt.getUTCFullYear()
    , dt.getUTCMonth()
    , dt.getUTCDate()
    , dt.getUTCHours()
    , dt.getUTCMinutes()
    , dt.getUTCSeconds()
    , dt.getUTCMilliseconds());
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.date.supportedFormats"></a>[module jake.date.supportedFormats](#apidoc.module.jake.date.supportedFormats)

#### <a name="apidoc.element.jake.date.supportedFormats.A"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>A (dt)](#apidoc.element.jake.date.supportedFormats.A)
- description and source-code
```javascript
A = function (dt) { return _this.weekdayLong[dt.getDay()]; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.B"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>B (dt)](#apidoc.element.jake.date.supportedFormats.B)
- description and source-code
```javascript
B = function (dt) { return _this.monthLong[dt.getMonth()]; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.C"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>C (dt)](#apidoc.element.jake.date.supportedFormats.C)
- description and source-code
```javascript
C = function (dt) { return _this.calcCentury(dt.getFullYear());; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.D"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>D (dt)](#apidoc.element.jake.date.supportedFormats.D)
- description and source-code
```javascript
D = function (dt) { return _this.strftime(dt, '%m/%d/%y') }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.F"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>F (dt)](#apidoc.element.jake.date.supportedFormats.F)
- description and source-code
```javascript
F = function (dt) { return _this.strftime(dt, '%Y-%m-%d');  }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.G"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>G ()](#apidoc.element.jake.date.supportedFormats.G)
- description and source-code
```javascript
G = function () { return _this.strftimeNotImplemented('G'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.H"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>H (dt)](#apidoc.element.jake.date.supportedFormats.H)
- description and source-code
```javascript
H = function (dt) { return string.lpad(dt.getHours(), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.I"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>I (dt)](#apidoc.element.jake.date.supportedFormats.I)
- description and source-code
```javascript
I = function (dt) { return string.lpad(
_this.hrMil2Std(dt.getHours()), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.M"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>M (dt)](#apidoc.element.jake.date.supportedFormats.M)
- description and source-code
```javascript
M = function (dt) { return string.lpad(dt.getMinutes(), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.R"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>R (dt)](#apidoc.element.jake.date.supportedFormats.R)
- description and source-code
```javascript
R = function (dt) { return _this.strftime(dt, '%H:%M'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.S"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>S (dt)](#apidoc.element.jake.date.supportedFormats.S)
- description and source-code
```javascript
S = function (dt) { return string.lpad(dt.getSeconds(), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.T"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>T (dt)](#apidoc.element.jake.date.supportedFormats.T)
- description and source-code
```javascript
T = function (dt) { return _this.strftime(dt, '%H:%M:%S'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.U"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>U ()](#apidoc.element.jake.date.supportedFormats.U)
- description and source-code
```javascript
U = function () { return _this.strftimeNotImplemented('U'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.V"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>V ()](#apidoc.element.jake.date.supportedFormats.V)
- description and source-code
```javascript
V = function () { return _this.strftimeNotImplemented('V'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.W"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>W ()](#apidoc.element.jake.date.supportedFormats.W)
- description and source-code
```javascript
W = function () { return _this.strftimeNotImplemented('W'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.X"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>X (dt)](#apidoc.element.jake.date.supportedFormats.X)
- description and source-code
```javascript
X = function (dt) { return _this.strftime(dt, '%T'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.Y"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>Y (dt)](#apidoc.element.jake.date.supportedFormats.Y)
- description and source-code
```javascript
Y = function (dt) { return string.lpad(dt.getFullYear(), '0', 4); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.Z"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>Z ()](#apidoc.element.jake.date.supportedFormats.Z)
- description and source-code
```javascript
Z = function () { return _this.strftimeNotImplemented('Z'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.a"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>a (dt)](#apidoc.element.jake.date.supportedFormats.a)
- description and source-code
```javascript
a = function (dt) { return _this.weekdayShort[dt.getDay()]; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.b"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>b (dt)](#apidoc.element.jake.date.supportedFormats.b)
- description and source-code
```javascript
b = function (dt) { return _this.monthShort[dt.getMonth()]; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.c"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>c (dt)](#apidoc.element.jake.date.supportedFormats.c)
- description and source-code
```javascript
c = function (dt) { return _this.strftime(dt, '%a %b %d %T %Y'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.d"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>d (dt)](#apidoc.element.jake.date.supportedFormats.d)
- description and source-code
```javascript
d = function (dt) { return string.lpad(dt.getDate(), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.e"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>e (dt)](#apidoc.element.jake.date.supportedFormats.e)
- description and source-code
```javascript
e = function (dt) { return string.lpad(dt.getDate(), ' ', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.f"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>f ()](#apidoc.element.jake.date.supportedFormats.f)
- description and source-code
```javascript
f = function () { return _this.strftimeNotImplemented('f'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.g"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>g ()](#apidoc.element.jake.date.supportedFormats.g)
- description and source-code
```javascript
g = function () { return _this.strftimeNotImplemented('g'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.h"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>h (dt)](#apidoc.element.jake.date.supportedFormats.h)
- description and source-code
```javascript
h = function (dt) { return _this.strftime(dt, '%b'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.j"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>j (dt)](#apidoc.element.jake.date.supportedFormats.j)
- description and source-code
```javascript
j = function (dt) { return string.lpad(
_this.calcDays(dt), '0', 3); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.k"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>k (dt)](#apidoc.element.jake.date.supportedFormats.k)
- description and source-code
```javascript
k = function (dt) { return string.lpad(dt.getHours(), ' ', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.l"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>l (dt)](#apidoc.element.jake.date.supportedFormats.l)
- description and source-code
```javascript
l = function (dt) { return string.lpad(
_this.hrMil2Std(dt.getHours()), ' ', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.m"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>m (dt)](#apidoc.element.jake.date.supportedFormats.m)
- description and source-code
```javascript
m = function (dt) { return string.lpad((dt.getMonth()+1), '0', 2); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.n"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>n ()](#apidoc.element.jake.date.supportedFormats.n)
- description and source-code
```javascript
n = function () { return '\n'; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.p"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>p (dt)](#apidoc.element.jake.date.supportedFormats.p)
- description and source-code
```javascript
p = function (dt) { return _this.getMeridian(dt.getHours()); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.r"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>r (dt)](#apidoc.element.jake.date.supportedFormats.r)
- description and source-code
```javascript
r = function (dt) { return _this.strftime(dt, '%I:%M:%S %p'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.t"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>t ()](#apidoc.element.jake.date.supportedFormats.t)
- description and source-code
```javascript
t = function () { return '\t'; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.u"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>u (dt)](#apidoc.element.jake.date.supportedFormats.u)
- description and source-code
```javascript
u = function (dt) { return _this.convertOneBase(dt.getDay()); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.w"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>w (dt)](#apidoc.element.jake.date.supportedFormats.w)
- description and source-code
```javascript
w = function (dt) { return dt.getDay(); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.x"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>x (dt)](#apidoc.element.jake.date.supportedFormats.x)
- description and source-code
```javascript
x = function (dt) { return _this.strftime(dt, '%D'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.y"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>y (dt)](#apidoc.element.jake.date.supportedFormats.y)
- description and source-code
```javascript
y = function (dt) { return _this.getTwoDigitYear(dt.getFullYear()); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.date.supportedFormats.z"></a>[function <span class="apidocSignatureSpan">jake.date.supportedFormats.</span>z ()](#apidoc.element.jake.date.supportedFormats.z)
- description and source-code
```javascript
z = function () { return _this.strftimeNotImplemented('z'); }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.i18n"></a>[module jake.i18n](#apidoc.module.jake.i18n)

#### <a name="apidoc.element.jake.i18n.I18n"></a>[function <span class="apidocSignatureSpan">jake.i18n.</span>I18n (locale)](#apidoc.element.jake.i18n.I18n)
- description and source-code
```javascript
I18n = function (locale) {
  var _locale = locale || i18n.getDefaultLocale();

  this.getLocale = function (locale) {
    return _locale;
  };

  this.setLocale = function (locale) {
    _locale = locale;
  };

  this.getText = function (key, opts, locale) {
    return i18n.getText(key,
        opts || {}, locale || _locale);
  };
  this.t = this.getText;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.i18n.getDefaultLocale"></a>[function <span class="apidocSignatureSpan">jake.i18n.</span>getDefaultLocale ()](#apidoc.element.jake.i18n.getDefaultLocale)
- description and source-code
```javascript
getDefaultLocale = function () {
  return _defaultLocale;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.i18n.getText"></a>[function <span class="apidocSignatureSpan">jake.i18n.</span>getText (key, opts, locale)](#apidoc.element.jake.i18n.getText)
- description and source-code
```javascript
getText = function (key, opts, locale) {
  var currentLocale = locale || _defaultLocale
    , currentLocaleStrings = _strings[currentLocale] || {}
    , defaultLocaleStrings = _strings[_defaultLocale] || {}
    , str = currentLocaleStrings[key]
          || defaultLocaleStrings[key] || "[[" + key + "]]";
  for (var p in opts) {
    str = str.replace(new RegExp('\\{' + p + '\\}', 'g'), opts[p]);
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.i18n.loadLocale"></a>[function <span class="apidocSignatureSpan">jake.i18n.</span>loadLocale (locale, strings)](#apidoc.element.jake.i18n.loadLocale)
- description and source-code
```javascript
loadLocale = function (locale, strings) {
  _strings[locale] = _strings[locale] || {};
  core.mixin(_strings[locale], strings);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.i18n.setDefaultLocale"></a>[function <span class="apidocSignatureSpan">jake.i18n.</span>setDefaultLocale (locale)](#apidoc.element.jake.i18n.setDefaultLocale)
- description and source-code
```javascript
setDefaultLocale = function (locale) {
  _defaultLocale = locale;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.inflection"></a>[module jake.inflection](#apidoc.module.jake.inflection)

#### <a name="apidoc.element.jake.inflection.parse"></a>[function <span class="apidocSignatureSpan">jake.inflection.</span>parse (type, word)](#apidoc.element.jake.inflection.parse)
- description and source-code
```javascript
parse = function (type, word) {
  var lowWord = word.toLowerCase()
    , inflections = this.inflections[type];

  if (this.inflections.uncountables[lowWord]) {
    return word;
  }

  var i = -1;
  while (++i < inflections.length) {
    var rule = inflections[i][0]
      , replacement = inflections[i][1];

    if (rule.test(word)) {
      return word.replace(rule, replacement)
    }
  }

  return word;
}
```
- example usage
```shell
...
      jake.errorCode = jake.errorCode || 1;
      process.exit(jake.errorCode);
    });
  });
};

this.parseArgs = function (args) {
  var result = (new parseargs.Parser(optsReg)).parse(args);
  this.setOpts(result.opts);
  this.setTaskNames(result.taskNames);
  this.setEnvVars(result.envVars);
};

this.setOpts = function (options) {
  var opts = options || {};
...
```

#### <a name="apidoc.element.jake.inflection.pluralize"></a>[function <span class="apidocSignatureSpan">jake.inflection.</span>pluralize (word)](#apidoc.element.jake.inflection.pluralize)
- description and source-code
```javascript
pluralize = function (word) {
  return self.parse('plurals', word);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.inflection.singularize"></a>[function <span class="apidocSignatureSpan">jake.inflection.</span>singularize (word)](#apidoc.element.jake.inflection.singularize)
- description and source-code
```javascript
singularize = function (word) {
  return self.parse('singulars', word);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.loader"></a>[module jake.loader](#apidoc.module.jake.loader)

#### <a name="apidoc.element.jake.loader.loadDirectory"></a>[function <span class="apidocSignatureSpan">jake.loader.</span>loadDirectory (d)](#apidoc.element.jake.loader.loadDirectory)
- description and source-code
```javascript
loadDirectory = function (d) {
  var dirname = d || 'jakelib'
    , dirlist;
  dirname = utils.file.absolutize(dirname);
  if (existsSync(dirname)) {
    dirlist = fs.readdirSync(dirname);
    dirlist.forEach(function (filePath) {
      if (JAKEFILE_PAT.test(filePath)) {
        if (/\.coffee$/.test(filePath)) {
          CoffeeScript = _requireCoffee();
        }
        if (/\.ls$/.test(filePath)) {
          LiveScript = _requireLiveScript();
        }
        require(path.join(dirname, filePath));
      }
    });
    return true;
  }

  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.loader.loadFile"></a>[function <span class="apidocSignatureSpan">jake.loader.</span>loadFile (file)](#apidoc.element.jake.loader.loadFile)
- description and source-code
```javascript
loadFile = function (file) {
  var jakefile = file ?
          file.replace(/\.js$/, '').replace(/\.coffee$/, '').replace(/\.ls/, '') : 'Jakefile'
    , fileSpecified = !!file
    // Dear God, why?
    , isCoffee = false
    , isLiveScript = false
    // Warning, recursive
    , exists
    , oldCwd = process.cwd();

  exists = function () {
    var cwd = process.cwd();
    if (existsSync(jakefile) || existsSync(jakefile + '.js') ||
      existsSync(jakefile + '.coffee') || existsSync(jakefile + '.ls')) {
      return true;
    }
    if (!fileSpecified) {
      process.chdir("..");
      if (cwd === process.cwd()) {
        // Restore the working directory on failure
        process.chdir(oldCwd);
        return false;
      }
      return exists();
    }
  };

  if (!exists()) {
    return false;
  }

  isCoffee = existsSync(jakefile + '.coffee');
  isLiveScript = existsSync(jakefile + '.ls');
  if (isCoffee) {
    CoffeeScript = _requireCoffee();
  }
  if (isLiveScript) {
      LiveScript = _requireLiveScript();
  }
  require(utils.file.absolutize(jakefile));
  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.log"></a>[module jake.log](#apidoc.module.jake.log)

#### <a name="apidoc.element.jake.log.log"></a>[function <span class="apidocSignatureSpan">jake.</span>log (obj)](#apidoc.element.jake.log.log)
- description and source-code
```javascript
log = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
...
  If you flag a task with this option, you must call the global
  'complete' method inside the task's action, for execution to proceed
  to the next task.

@example
desc('This is the default task.');
task('default', function (params) {
  console.log('This is the default task.');
});

desc('This task has prerequisites.');
task('hasPrereqs', ['foo', 'bar', 'baz'], function (params) {
  console.log('Ran some prereqs first.');
});
...
```

#### <a name="apidoc.element.jake.log.access"></a>[function <span class="apidocSignatureSpan">jake.log.</span>access (obj)](#apidoc.element.jake.log.access)
- description and source-code
```javascript
access = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.alert"></a>[function <span class="apidocSignatureSpan">jake.log.</span>alert (obj)](#apidoc.element.jake.log.alert)
- description and source-code
```javascript
alert = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.critical"></a>[function <span class="apidocSignatureSpan">jake.log.</span>critical (obj)](#apidoc.element.jake.log.critical)
- description and source-code
```javascript
critical = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.debug"></a>[function <span class="apidocSignatureSpan">jake.log.</span>debug (obj)](#apidoc.element.jake.log.debug)
- description and source-code
```javascript
debug = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.emergency"></a>[function <span class="apidocSignatureSpan">jake.log.</span>emergency (obj)](#apidoc.element.jake.log.emergency)
- description and source-code
```javascript
emergency = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.error"></a>[function <span class="apidocSignatureSpan">jake.log.</span>error (obj)](#apidoc.element.jake.log.error)
- description and source-code
```javascript
error = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
...
var msg;

if (jake.listeners('error').length) {
  jake.emit('error', err);
  return;
}

utils.logger.error('jake aborted.');
if (this.opts.trace && err.stack) {
  utils.logger.error(err.stack);
}
else {
  if (err.stack) {
    msg = err.stack.split('\n').slice(0, 3).join('\n');
    utils.logger.error(msg);
...
```

#### <a name="apidoc.element.jake.log.info"></a>[function <span class="apidocSignatureSpan">jake.log.</span>info (obj)](#apidoc.element.jake.log.info)
- description and source-code
```javascript
info = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.notice"></a>[function <span class="apidocSignatureSpan">jake.log.</span>notice (obj)](#apidoc.element.jake.log.notice)
- description and source-code
```javascript
notice = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.registerLogger"></a>[function <span class="apidocSignatureSpan">jake.log.</span>registerLogger (logger)](#apidoc.element.jake.log.registerLogger)
- description and source-code
```javascript
registerLogger = function (logger) {
  // Malkovitch, Malkovitch
  if (logger === log) {
    return;
  }
  _logger = logger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.warn"></a>[function <span class="apidocSignatureSpan">jake.log.</span>warn (obj)](#apidoc.element.jake.log.warn)
- description and source-code
```javascript
warn = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.log.warning"></a>[function <span class="apidocSignatureSpan">jake.log.</span>warning (obj)](#apidoc.element.jake.log.warning)
- description and source-code
```javascript
warning = function (obj) {
  _output(obj, p);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.logger"></a>[module jake.logger](#apidoc.module.jake.logger)

#### <a name="apidoc.element.jake.logger.error"></a>[function <span class="apidocSignatureSpan">jake.logger.</span>error (out)](#apidoc.element.jake.logger.error)
- description and source-code
```javascript
error = function (out) {
  _output('error', out);
}
```
- example usage
```shell
...
var msg;

if (jake.listeners('error').length) {
  jake.emit('error', err);
  return;
}

utils.logger.error('jake aborted.');
if (this.opts.trace && err.stack) {
  utils.logger.error(err.stack);
}
else {
  if (err.stack) {
    msg = err.stack.split('\n').slice(0, 3).join('\n');
    utils.logger.error(msg);
...
```

#### <a name="apidoc.element.jake.logger.log"></a>[function <span class="apidocSignatureSpan">jake.logger.</span>log (out)](#apidoc.element.jake.logger.log)
- description and source-code
```javascript
log = function (out) {
  _output('log', out);
}
```
- example usage
```shell
...
  If you flag a task with this option, you must call the global
  'complete' method inside the task's action, for execution to proceed
  to the next task.

@example
desc('This is the default task.');
task('default', function (params) {
  console.log('This is the default task.');
});

desc('This task has prerequisites.');
task('hasPrereqs', ['foo', 'bar', 'baz'], function (params) {
  console.log('Ran some prereqs first.');
});
...
```



# <a name="apidoc.module.jake.namespace"></a>[module jake.namespace](#apidoc.module.jake.namespace)

#### <a name="apidoc.element.jake.namespace.Namespace"></a>[function <span class="apidocSignatureSpan">jake.namespace.</span>Namespace (name, parentNamespace)](#apidoc.element.jake.namespace.Namespace)
- description and source-code
```javascript
Namespace = function (name, parentNamespace) {
  this.name = name;
  this.parentNamespace = parentNamespace;
  this.childNamespaces = {};
  this.tasks = {};
  this.rules = {};
  this.path = this.getPath();
}
```
- example usage
```shell
...
    task('clobber', function () {
      // Clobber the doc directory first
    });
  });
 */
this.namespace = function (name, closure) {
  var curr = jake.currentNamespace
    , ns = curr.childNamespaces[name] || new jake.Namespace(name, curr);
  curr.childNamespaces[name] = ns;
  jake.currentNamespace = ns;
  closure();
  jake.currentNamespace = curr;
  jake.currentTaskDescription = null;
  return ns;
};
...
```



# <a name="apidoc.module.jake.network"></a>[module jake.network](#apidoc.module.jake.network)

#### <a name="apidoc.element.jake.network.isPortOpen"></a>[function <span class="apidocSignatureSpan">jake.network.</span>isPortOpen (port, host, callback)](#apidoc.element.jake.network.isPortOpen)
- description and source-code
```javascript
isPortOpen = function (port, host, callback) {
		if (typeof host === 'function' && !callback) {
			callback = host;
			host = 'localhost';
		}

		var isOpen = false
			, connection
			, error;

		connection = net.createConnection(port, host, function () {
			isOpen = true;
			connection.end();
		});

		connection.on('error', function (err) {
			// We ignore 'ECONNREFUSED' as it simply indicates the port isn't open.
			// Anything else is reported
			if(err.code !== 'ECONNREFUSED') {
				error = err;
			}
		});

		connection.setTimeout(400, function () {
			connection.end();
		});

		connection.on('close', function () {
			callback && callback(error, isOpen);
		});
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.object"></a>[module jake.object](#apidoc.module.jake.object)

#### <a name="apidoc.element.jake.object.isEmpty"></a>[function <span class="apidocSignatureSpan">jake.object.</span>isEmpty (object)](#apidoc.element.jake.object.isEmpty)
- description and source-code
```javascript
isEmpty = function (object) {
  // Returns true if a object is empty false if not
  for (var i in object) { return false; }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.object.merge"></a>[function <span class="apidocSignatureSpan">jake.object.</span>merge (object, otherObject)](#apidoc.element.jake.object.merge)
- description and source-code
```javascript
merge = function (object, otherObject) {
  var obj = object || {}
    , otherObj = otherObject || {}
    , key, value;

  for (key in otherObj) {
    value = otherObj[key];

    // Check if a value is an Object, if so recursively add it's key/values
    if (typeof value === 'object' && !(value instanceof Array)) {
      // Update value of object to the one from otherObj
      obj[key] = this.merge(obj[key], value);
    }
    // Value is anything other than an Object, so just add it
    else {
      obj[key] = value;
    }
  }

  return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.object.reverseMerge"></a>[function <span class="apidocSignatureSpan">jake.object.</span>reverseMerge (object, defaultObject)](#apidoc.element.jake.object.reverseMerge)
- description and source-code
```javascript
reverseMerge = function (object, defaultObject) {
  // Same as 'merge' except 'defaultObject' is the object being changed
  // - this is useful if we want to easily deal with default object values
  return this.merge(defaultObject, object);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.object.toArray"></a>[function <span class="apidocSignatureSpan">jake.object.</span>toArray (object)](#apidoc.element.jake.object.toArray)
- description and source-code
```javascript
toArray = function (object) {
  // Converts an object into an array of objects with the original key, values
  array = [];

  for (var i in object) {
    array.push({ key: i, value: object[i] });
  }

  return array;
}
```
- example usage
```shell
...
  definition.call(this);
}

desc('Runs these tasks: ' + this.watchTasks.join(', '));
task(name, function () {
  console.log('WatchTask started for: ' + self.watchTasks.join(', '));
  jake.watch('.', {includePattern: /.+/}, function (filePath) {
    var fileMatch = self.watchFiles.toArray().some(function (item) {
      return item == filePath;
    });
    if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
      last = (new Date()).getTime();
      self.rootTask.reenable(true);
      self.rootTask.invoke();
    }
...
```



# <a name="apidoc.module.jake.package_task"></a>[module jake.package_task](#apidoc.module.jake.package_task)

#### <a name="apidoc.element.jake.package_task.PackageTask"></a>[function <span class="apidocSignatureSpan">jake.package_task.</span>PackageTask ()](#apidoc.element.jake.package_task.PackageTask)
- description and source-code
```javascript
PackageTask = function () {
  var args = Array.prototype.slice.call(arguments)
    , name = args.shift()
    , version = args.shift()
    , definition = args.pop()
    , prereqs = args.pop() || []; // Optional

    prereqs = [].concat(prereqs); // Accept string or list

<span class="apidocCodeCommentSpan">  /**
    @name jake.PackageTask#name
    @public
    @type {String}
    @description The name of the project
   */
</span>  this.name = name;
  /**
    @name jake.PackageTask#version
    @public
    @type {String}
    @description The project version-string
   */
  this.version = version;
  /**
    @name jake.PackageTask#prereqs
    @public
    @type {Array}
    @description Tasks to run before packaging
   */
  this.prereqs = prereqs;
  /**
    @name jake.PackageTask#version
    @public
    @type {String='pkg'}
    @description The directory-name to use for packaging the software
   */
  this.packageDir = 'pkg';
  /**
    @name jake.PackageTask#packageFiles
    @public
    @type {jake.FileList}
    @description The list of files and directories to include in the
    package-archive
   */
  this.packageFiles = new FileList();
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tgz archive of the package
   */
  this.needTar = false;
  /**
    @name jake.PackageTask#needTar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a gzip .tar.gz archive of the package
   */
  this.needTarGz = false;
  /**
    @name jake.PackageTask#needTarBz2
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'tar' utility to create
    a bzip2 .bz2 archive of the package
   */
  this.needTarBz2 = false;
  /**
    @name jake.PackageTask#needJar
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'jar' utility to create
    a .jar archive of the package
   */
  this.needJar = false;
  /**
    @name jake.PackageTask#needZip
    @public
    @type {Boolean=false}
    @description If set to true, uses the 'zip' utility to create
    a .zip archive of the package
   */
  this.needZip = false;
  /**
    @name jake.PackageTask#manifestFile
    @public
    @type {String=null}
    @description Can be set to point the 'jar' utility at a manifest
    file to use in a .jar archive. If unset, one will be automatically
    created by the 'jar' utility. This path should be relative to the
    root of the package directory (this.packageDir above, likely 'pkg')
   */
  this.manifestFile = null;
  /**
    @name jake.PackageTask#tarCommand
    @public
    @type {String='tar'}
    @description The shell-command to use for creating tar archives.
   */
  this.tarCommand = 'tar';
  /**
    @name jake.PackageTask#jarCommand
    @public
    @type {String='jar'}
    @description The shell-command to use for creating jar archives.
   */
  this.jarCommand = 'jar';
  /**
    @name jake.PackageTask#zipCommand
    @public
    @type {String='zip'}
    @description The shell-command to use for creating zip archives.
   */
  this.zipCommand = 'zip';
  /**
    @name jake.PackageTask#archiveNoBaseDir
    @public
    @type {Boolean=false}
    @description Simple option for performing the archive on the
    contents of the directory instead of the directory itself
   */
  this.archiveNoBaseDir = false;
  /**
    @name jake.PackageTask#archiveChangeDir
    @public
    @type {String=null}
    @description Equivalent to the '-C' command for the 'tar' and 'jar'
    commands. ("Change to this directory before adding files.")
   */
  this.archiveChangeDir = null;
  /**
    @name jake.PackageTask#archiveContentDir
    @public
    @type {String=null}
    @description Specifies the files and directories to include in the
    package-archive. If unset, this will default to the main package
    directory -- i.e., name + version.
   */
  this.archiveContentDir = null;

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
  }
  else {
    throw new Error();
  }
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
...
```



# <a name="apidoc.module.jake.parseargs"></a>[module jake.parseargs](#apidoc.module.jake.parseargs)

#### <a name="apidoc.element.jake.parseargs.Parser"></a>[function <span class="apidocSignatureSpan">jake.parseargs.</span>Parser (opts)](#apidoc.element.jake.parseargs.Parser)
- description and source-code
```javascript
Parser = function (opts) {
  // A key/value object of matching options parsed out of the args
  this.opts = {};
  this.taskNames = null;
  this.envVars = null;

  // Data structures used for parsing
  this.reg = [];
  this.shortOpts = {};
  this.longOpts = {};

  var item;
  for (var i = 0, ii = opts.length; i < ii; i++) {
    item = opts[i];
    this.shortOpts[item.abbr] = item;
    this.longOpts[item.full] = item;
  }
  this.reg = opts;
}
```
- example usage
```shell
...
      jake.errorCode = jake.errorCode || 1;
      process.exit(jake.errorCode);
    });
  });
};

this.parseArgs = function (args) {
  var result = (new parseargs.Parser(optsReg)).parse(args);
  this.setOpts(result.opts);
  this.setTaskNames(result.taskNames);
  this.setEnvVars(result.envVars);
};

this.setOpts = function (options) {
  var opts = options || {};
...
```



# <a name="apidoc.module.jake.program"></a>[module jake.program](#apidoc.module.jake.program)

#### <a name="apidoc.element.jake.program.Program"></a>[function <span class="apidocSignatureSpan">jake.program.</span>Program ()](#apidoc.element.jake.program.Program)
- description and source-code
```javascript
Program = function () {
  this.opts = {};
  this.taskNames = null;
  this.taskArgs = null;
  this.envVars = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.publish_task"></a>[module jake.publish_task](#apidoc.module.jake.publish_task)

#### <a name="apidoc.element.jake.publish_task.PublishTask"></a>[function <span class="apidocSignatureSpan">jake.publish_task.</span>PublishTask ()](#apidoc.element.jake.publish_task.PublishTask)
- description and source-code
```javascript
PublishTask = function () {
  var args = Array.prototype.slice.call(arguments).filter(function (item) {
        return typeof item != 'undefined';
      })
    , arg
    , opts = {}
    , definition
    , prereqs = []
    , createDef = function (arg) {
        return function () {
          this.packageFiles.include(arg);
        };
      };

  this.name = args.shift();

  // Old API, just name + list of files
  if (args.length == 1 && (Array.isArray(args[0]) || typeof args[0] == 'string')) {
    definition = createDef(args.pop());
  }
  // Current API, name + [prereqs] + [opts] + definition
  else {
    while ((arg = args.pop())) {
      // Definition func
      if (typeof arg == 'function') {
        definition = arg;
      }
      // Prereqs
      else if (Array.isArray(arg) || typeof arg == 'string') {
        prereqs = arg;
      }
      // Opts
      else {
        opts = arg;
      }
    }
  }

  this.prereqs = prereqs;
  this.packageFiles = new FileList();
  this.publishCmd = opts.publishCmd || 'npm publish %filename';
  this.publishMessage = opts.publishMessage || 'BOOM! Published.';
  this.gitCmd = opts.gitCmd || 'git';
  this.versionFiles = opts.versionFiles || ['package.json'];
  this.scheduleDelay = 5000;

  // Override utility funcs for testing
  this._ensureRepoClean = function (stdout) {
    if (stdout.length) {
      fail(new Error('Git repository is not clean.'));
    }
  };
  this._getCurrentBranch = function (stdout) {
    return utils.string.trim(stdout);
  };

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
}
```
- example usage
```shell
...
};

this.packageTask = function (name, version, definition) {
  return new jake.PackageTask(name, version, definition);
};

this.publishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

// Backward-compat
this.npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};
...
```



# <a name="apidoc.module.jake.rule"></a>[module jake.rule](#apidoc.module.jake.rule)

#### <a name="apidoc.element.jake.rule.Rule"></a>[function <span class="apidocSignatureSpan">jake.rule.</span>Rule (opts)](#apidoc.element.jake.rule.Rule)
- description and source-code
```javascript
Rule = function (opts) {
  this.pattern = opts.pattern;
  this.source = opts.source;
  this.prereqs = opts.prereqs;
  this.action = opts.action;
  this.opts = opts.opts;
  this.desc =  opts.desc;
  this.ns = opts.ns;
}
```
- example usage
```shell
...
    prereqs = arg;
  }
  else {
    opts = arg;
  }
}

jake.currentNamespace.rules[key] = new jake.Rule({
  pattern: pattern
, source: source
, prereqs: prereqs
, action: action
, opts: opts
, desc: jake.currentTaskDescription
, ns: jake.currentNamespace
...
```



# <a name="apidoc.module.jake.string"></a>[module jake.string](#apidoc.module.jake.string)

#### <a name="apidoc.element.jake.string.camelize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>camelize (string, options)](#apidoc.element.jake.string.camelize)
- description and source-code
```javascript
camelize = function (string, options) {
  var str = string || ''
    , ret
    , config = {
        initialCap: false
      , leadingUnderscore: false
      }
    , opts = options || {};

  str = String(str);

  // Backward-compat
  if (typeof opts == 'boolean') {
    config = {
      initialCap: true
    };
  }
  else {
    core.mixin(config, opts);
  }

  ret = str.replace(repl, function (m, m1) {
    return m1.toUpperCase();
  });

  if (config.leadingUnderscore & str.indexOf('_') === 0) {
    ret = '_' + this.decapitalize(ret);
  }
  // If initialCap is true capitalize it
  ret = config.initialCap ? this.capitalize(ret) : this.decapitalize(ret);

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.capitalize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>capitalize (string)](#apidoc.element.jake.string.capitalize)
- description and source-code
```javascript
capitalize = function (string) {
  var str = string || '';
  str = String(str);

  return str.substr(0, 1).toUpperCase() + str.substr(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.chomp"></a>[function <span class="apidocSignatureSpan">jake.string.</span>chomp (string, character)](#apidoc.element.jake.string.chomp)
- description and source-code
```javascript
chomp = function (string, character) {
  var str = string || ''
    , pat = character ? new RegExp(character + '+$') : _RTR;
  str = String(str);

  return str.replace(pat, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.chop"></a>[function <span class="apidocSignatureSpan">jake.string.</span>chop (string)](#apidoc.element.jake.string.chop)
- description and source-code
```javascript
chop = function (string) {
  var index
    , str = string || '';
  str = String(str);

  if (str.length) {
    // Special-case for \r\n
    index = str.indexOf('\r\n');
    if (index == str.length - 2) {
      return str.substring(0, index);
    }
    return str.substring(0, str.length - 1);
  }
  else {
    return '';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.dasherize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>dasherize (string, replace)](#apidoc.element.jake.string.dasherize)
- description and source-code
```javascript
dasherize = function (string, replace) {
  var repl = replace || '-'
  return this.snakeize(string, repl);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.decamelize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>decamelize (string, separ)](#apidoc.element.jake.string.decamelize)
- description and source-code
```javascript
decamelize = function (string, separ) {
  var str = string || ''
    , sep = separ || '_'
    , leading = separ ? new RegExp('^' + sep, 'g') : lead;
  str = String(str);
  return str.replace(repl, sep + '$1').toLowerCase().
    replace(leading, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.decapitalize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>decapitalize (string)](#apidoc.element.jake.string.decapitalize)
- description and source-code
```javascript
decapitalize = function (string) {
  var str = string || '';
  str = String(str);

  return str.substr(0, 1).toLowerCase() + str.substr(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.escapeRegExpChars"></a>[function <span class="apidocSignatureSpan">jake.string.</span>escapeRegExpChars (string)](#apidoc.element.jake.string.escapeRegExpChars)
- description and source-code
```javascript
escapeRegExpChars = function (string) {
  var str = string || '';
  str = String(str);
  return str.replace(sRE, '\\$1');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.escapeXML"></a>[function <span class="apidocSignatureSpan">jake.string.</span>escapeXML (str)](#apidoc.element.jake.string.escapeXML)
- description and source-code
```javascript
escapeXML = function (str) {
  var string = str;

  // If string is NaN, null or undefined then provide an empty default
  if((typeof string === 'undefined') ||
      string === null ||
      (!string && isNaN(string))) {
    string = '';
  }
  string = string.toString();

  var from, to, p;
  for (p in _CHARS) {
    from = direction == 'to' ? p : _CHARS[p];
    to = direction == 'to' ? _CHARS[p] : p;

    string = string.replace(new RegExp(from, 'gm'), to);
  }

  return string;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.getInflection"></a>[function <span class="apidocSignatureSpan">jake.string.</span>getInflection (name, key, pluralization)](#apidoc.element.jake.string.getInflection)
- description and source-code
```javascript
getInflection = function (name, key, pluralization) {
  var infl = this.getInflections(name);
  return infl[key][pluralization];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.getInflections"></a>[function <span class="apidocSignatureSpan">jake.string.</span>getInflections (name)](#apidoc.element.jake.string.getInflections)
- description and source-code
```javascript
getInflections = function (name) {
  if (!name) {
    return;
  }

  var self = this
      // Use plural version to fix possible mistakes(e,g,. thingie instead of thingy)
    , normalizedName = this.snakeize(inflection.pluralize(name))
    , nameSingular = inflection.singularize(normalizedName)
    , namePlural = inflection.pluralize(normalizedName)
    , nameNormal = this.snakeize(name);

  return {
    // For filepaths or URLs
    filename: {
      normal: nameNormal
      // neil_peart
    , singular: nameSingular
      // neil_pearts
    , plural: namePlural
    }
    // Constructor names
  , constructor: {
      normal: self.camelize(nameNormal, {initialCap: true})
      // NeilPeart
    , singular: self.camelize(nameSingular, {initialCap: true})
      // NeilPearts
    , plural: self.camelize(namePlural, {initialCap: true})
    }
  , property: {
      normal: self.camelize(nameNormal)
      // neilPeart
    , singular: self.camelize(nameSingular)
      // neilPearts
    , plural: self.camelize(namePlural)
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.include"></a>[function <span class="apidocSignatureSpan">jake.string.</span>include (searchIn, searchFor)](#apidoc.element.jake.string.include)
- description and source-code
```javascript
include = function (searchIn, searchFor) {
  var str = searchFor;
  if (!str && typeof string != 'string') {
    return false;
  }
  str = String(str);
  return (searchIn.indexOf(str) > -1);
}
```
- example usage
```shell
...
  , 'package.json'
  , 'app/*'
  , 'bin/*'
  , 'config/*'
  , 'lib/*'
  , 'node_modules/*'
  ];
  this.packageFiles.include(files);
  this.packageFiles.exclude('node_modules/foobar');
  this.needTarGz = true;
});

 */
var PackageTask = function () {
var args = Array.prototype.slice.call(arguments)
...
```

#### <a name="apidoc.element.jake.string.lpad"></a>[function <span class="apidocSignatureSpan">jake.string.</span>lpad (string, character, width)](#apidoc.element.jake.string.lpad)
- description and source-code
```javascript
lpad = function (string, character, width) {
  var str = string || ''
    , width;
  str = String(str);

  // Should width be string.length + 1? or the same to be safe
  width = parseInt(width, 10) || str.length;
  character = character || ' ';

  while (str.length < width) {
    str = character + str;
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.ltrim"></a>[function <span class="apidocSignatureSpan">jake.string.</span>ltrim (string, character)](#apidoc.element.jake.string.ltrim)
- description and source-code
```javascript
ltrim = function (string, character) {
  var str = string || ''
    , pat = character ? new RegExp('^' + character + '+') : _LTR;
  str = String(str);

  return str.replace(pat, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.needsEscape"></a>[function <span class="apidocSignatureSpan">jake.string.</span>needsEscape (string)](#apidoc.element.jake.string.needsEscape)
- description and source-code
```javascript
needsEscape = function (string) {
  var pat = ''
    , p;

  for (p in _CHARS) {
    pat += direction == 'to' ? p : _CHARS[p];
    pat += '|';
  }

  pat = pat.substr(0, pat.length - 1);
  pat = new RegExp(pat, "gm");
  return pat.test(string)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.needsUnescape"></a>[function <span class="apidocSignatureSpan">jake.string.</span>needsUnescape (string)](#apidoc.element.jake.string.needsUnescape)
- description and source-code
```javascript
needsUnescape = function (string) {
  var pat = ''
    , p;

  for (p in _CHARS) {
    pat += direction == 'to' ? p : _CHARS[p];
    pat += '|';
  }

  pat = pat.substr(0, pat.length - 1);
  pat = new RegExp(pat, "gm");
  return pat.test(string)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.nl2br"></a>[function <span class="apidocSignatureSpan">jake.string.</span>nl2br (string)](#apidoc.element.jake.string.nl2br)
- description and source-code
```javascript
nl2br = function (string) {
  var str = string || '';
  str = String(str);

  return str.replace(_NL,'<br />');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.pad"></a>[function <span class="apidocSignatureSpan">jake.string.</span>pad (string, character, width)](#apidoc.element.jake.string.pad)
- description and source-code
```javascript
pad = function (string, character, width) {
  var str = string || ''
    , width;
  str = String(str);

  // Should width be string.length + 1? or the same to be safe
  width = parseInt(width, 10) || str.length;
  character = character || ' ';

  while (str.length < width) {
    str = character + str + character;
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.reverse"></a>[function <span class="apidocSignatureSpan">jake.string.</span>reverse (string)](#apidoc.element.jake.string.reverse)
- description and source-code
```javascript
reverse = function (string) {
  var str = string || '';
  str = String(str);
  return this.toArray(str).reverse().join('');
}
```
- example usage
```shell
...
    var parts = []
      , next = this;
    while (!!next) {
      parts.push(next.name);
      next = next.parentNamespace;
    }
    parts.pop(); // Remove 'default'
    return parts.reverse().join(':');
  };

})();

module.exports.Namespace = Namespace;
...
```

#### <a name="apidoc.element.jake.string.rpad"></a>[function <span class="apidocSignatureSpan">jake.string.</span>rpad (string, character, width)](#apidoc.element.jake.string.rpad)
- description and source-code
```javascript
rpad = function (string, character, width) {
  var str = string || ''
    , width;
  str = String(str);

  // Should width be string.length + 1? or the same to be safe
  width = parseInt(width, 10) || str.length;
  character = character || ' ';

  while (str.length < width) {
    str += character;
  }
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.rtrim"></a>[function <span class="apidocSignatureSpan">jake.string.</span>rtrim (string, character)](#apidoc.element.jake.string.rtrim)
- description and source-code
```javascript
rtrim = function (string, character) {
  var str = string || ''
    , pat = character ? new RegExp(character + '+$') : _RTR;
  str = String(str);

  return str.replace(pat, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.snakeize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>snakeize (string, separ)](#apidoc.element.jake.string.snakeize)
- description and source-code
```javascript
snakeize = function (string, separ) {
  var str = string || ''
    , sep = separ || '_'
    , leading = separ ? new RegExp('^' + sep, 'g') : lead;
  str = String(str);
  return str.replace(repl, sep + '$1').toLowerCase().
    replace(leading, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.stripTags"></a>[function <span class="apidocSignatureSpan">jake.string.</span>stripTags (string, allowed)](#apidoc.element.jake.string.stripTags)
- description and source-code
```javascript
stripTags = function (string, allowed) {
  // taken from http://phpjs.org/functions/strip_tags/
  var allowed = (((allowed || "") + "").toLowerCase().match(/<[a-z][a-z0-9]*>/g) || []).join(''); // making sure the allowed arg
 is a string containing only tags in lowercase (<a><b><c>)
  var tags = /<\/?([a-z][a-z0-9]*)\b[^>]*>/gi,
  comments = /<!--[\s\S]*?-->/gi;
  return string.replace(comments, '').replace(tags, function ($0, $1) {
    return allowed.indexOf('<' + $1.toLowerCase() + '>') > -1 ? $0 : '';
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.toArray"></a>[function <span class="apidocSignatureSpan">jake.string.</span>toArray (string)](#apidoc.element.jake.string.toArray)
- description and source-code
```javascript
toArray = function (string) {
  var str = string || ''
    , arr = []
    , i = -1;
  str = String(str);

  while (++i < str.length) {
    arr.push(str.substr(i, 1));
  }

  return arr;
}
```
- example usage
```shell
...
  definition.call(this);
}

desc('Runs these tasks: ' + this.watchTasks.join(', '));
task(name, function () {
  console.log('WatchTask started for: ' + self.watchTasks.join(', '));
  jake.watch('.', {includePattern: /.+/}, function (filePath) {
    var fileMatch = self.watchFiles.toArray().some(function (item) {
      return item == filePath;
    });
    if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
      last = (new Date()).getTime();
      self.rootTask.reenable(true);
      self.rootTask.invoke();
    }
...
```

#### <a name="apidoc.element.jake.string.trim"></a>[function <span class="apidocSignatureSpan">jake.string.</span>trim (string, character)](#apidoc.element.jake.string.trim)
- description and source-code
```javascript
trim = function (string, character) {
  var str = string || ''
    , pat = character ? new RegExp('^' + character + '+|' + character + '+$', 'g') : _TR;
  str = String(str);

  return str.replace(pat, '');
}
```
- example usage
```shell
...
  // Override utility funcs for testing
  this._ensureRepoClean = function (stdout) {
    if (stdout.length) {
      fail(new Error('Git repository is not clean.'));
    }
  };
  this._getCurrentBranch = function (stdout) {
    return utils.string.trim(stdout);
  };

  if (typeof definition == 'function') {
    definition.call(this);
  }
  this.define();
};
...
```

#### <a name="apidoc.element.jake.string.truncate"></a>[function <span class="apidocSignatureSpan">jake.string.</span>truncate (string, options, callback)](#apidoc.element.jake.string.truncate)
- description and source-code
```javascript
truncate = function (string, options, callback) {
  var str = string || ''
    , stringLen
    , opts
    , stringLenWithOmission
    , last
    , ignoreCase
    , multiLine
    , stringToWorkWith
    , lastIndexOf
    , nextStop
    , result
    , returnString;

  str = String(str);
  stringLen = str.length

  // If 'options' is a number, assume it's the length and
  // create a options object with length
  if (typeof options === 'number') {
    opts = {
      length: options
    };
  }
  else {
    opts = options || {};
  }

  // Set 'opts' defaults
  opts.length = opts.length || stringLen;
  opts.omission = opts.omission || opts.ellipsis || '...';

  stringLenWithOmission = opts.length - opts.omission.length;

  // Set the index to stop at for 'string'
  if (opts.seperator) {
    if (opts.seperator instanceof RegExp) {
      // If 'seperator' is a regex
      if (opts.seperator.global) {
        opts.seperator = opts.seperator;
      } else {
        ignoreCase = opts.seperator.ignoreCase ? 'i' : ''
        multiLine = opts.seperator.multiLine ? 'm' : '';
        opts.seperator = new RegExp(opts.seperator.source,
            'g' + ignoreCase + multiLine);
      }
      stringToWorkWith = str.substring(0, stringLenWithOmission + 1)
      lastIndexOf = -1
      nextStop = 0

      while ((result = opts.seperator.exec(stringToWorkWith))) {
        lastIndexOf = result.index;
        opts.seperator.lastIndex = ++nextStop;
      }
      last = lastIndexOf;
    }
    else {
      // Seperator is a String
      last = str.lastIndexOf(opts.seperator, stringLenWithOmission);
    }

    // If the above couldn't be found, they'll default to -1 so,
    // we need to just set it as 'stringLenWithOmission'
    if (last === -1) {
      last = stringLenWithOmission;
    }
  }
  else {
    last = stringLenWithOmission;
  }

  if (stringLen < opts.length) {
    return str;
  }
  else {
    returnString = str.substring(0, last) + opts.omission;
    returnString += callback && typeof callback === 'function' ? callback() : '';
    return returnString;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.truncateHTML"></a>[function <span class="apidocSignatureSpan">jake.string.</span>truncateHTML (string, options, callback)](#apidoc.element.jake.string.truncateHTML)
- description and source-code
```javascript
truncateHTML = function (string, options, callback) {
  var str = string || ''
    , returnString = ''
    , opts = options;

  str = String(str);

  // If 'options' is a number assume it's the length and create a options object with length
  if (typeof opts === 'number') {
    var num = opts;

    opts = {};
    opts.length = num;
  } else opts = opts || {};

  // Set 'default' options for HTML specifics
  opts.once = opts.once || false;

  var pat = /(<[^>]*>)/ // Patter for matching HTML tags
    , arr = [] // Holds the HTML tags and content seperately
    , truncated = false
    , result = pat.exec(str)
    , item
    , firstPos
    , lastPos
    , i;

  // Gather the HTML tags and content into the array
  while (result) {
    firstPos = result.index;
    lastPos = pat.lastIndex;

    if (firstPos !== 0) {
      // Should be content not HTML tags
      arr.push(str.substring(0, firstPos));
      // Slice content from string
      str = str.slice(firstPos);
    }

    arr.push(result[0]); // Push HTML tags
    str = str.slice(result[0].length);

    // Re-run the pattern on the new string
    result = pat.exec(str);
  }
  if (str !== '') {
    arr.push(str);
  }

  // Loop through array items appending the tags to the string,
  // - and truncating the text then appending it to content
  i = -1;
  while (++i < arr.length) {
    item = arr[i];
    switch (true) {
      // Closing tag
      case item.indexOf('</') == 0:
        returnString += item;
        openTag = null;
        break;
      // Opening tag
      case item.indexOf('<') == 0:
        returnString += item;
        openTag = item;
        break;
      // Normal text
      default:
        if (opts.once && truncated) {
          returnString += item;
        } else {
          returnString += this.truncate(item, opts, callback);
          truncated = true;
        }
        break;
    }
  }

  return returnString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.underscoreize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>underscoreize (string, separ)](#apidoc.element.jake.string.underscoreize)
- description and source-code
```javascript
underscoreize = function (string, separ) {
  var str = string || ''
    , sep = separ || '_'
    , leading = separ ? new RegExp('^' + sep, 'g') : lead;
  str = String(str);
  return str.replace(repl, sep + '$1').toLowerCase().
    replace(leading, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.underscorize"></a>[function <span class="apidocSignatureSpan">jake.string.</span>underscorize (string, separ)](#apidoc.element.jake.string.underscorize)
- description and source-code
```javascript
underscorize = function (string, separ) {
  var str = string || ''
    , sep = separ || '_'
    , leading = separ ? new RegExp('^' + sep, 'g') : lead;
  str = String(str);
  return str.replace(repl, sep + '$1').toLowerCase().
    replace(leading, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.unescapeXML"></a>[function <span class="apidocSignatureSpan">jake.string.</span>unescapeXML (str)](#apidoc.element.jake.string.unescapeXML)
- description and source-code
```javascript
unescapeXML = function (str) {
  var string = str;

  // If string is NaN, null or undefined then provide an empty default
  if((typeof string === 'undefined') ||
      string === null ||
      (!string && isNaN(string))) {
    string = '';
  }
  string = string.toString();

  var from, to, p;
  for (p in _CHARS) {
    from = direction == 'to' ? p : _CHARS[p];
    to = direction == 'to' ? _CHARS[p] : p;

    string = string.replace(new RegExp(from, 'gm'), to);
  }

  return string;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.string.uuid"></a>[function <span class="apidocSignatureSpan">jake.string.</span>uuid (length, radix)](#apidoc.element.jake.string.uuid)
- description and source-code
```javascript
uuid = function (length, radix) {
  var chars = _UUID_CHARS
    , uuid = []
    , r
    , i;

  radix = radix || chars.length;

  if (length) {
    // Compact form
    i = -1;
    while (++i < length) {
      uuid[i] = chars[0 | Math.random()*radix];
    }
  } else {
    // rfc4122, version 4 form

    // rfc4122 requires these characters
    uuid[8] = uuid[13] = uuid[18] = uuid[23] = '-';
    uuid[14] = '4';

    // Fill in random data.  At i==19 set the high bits of clock sequence as
    // per rfc4122, sec. 4.1.5
    i = -1;
    while (++i < 36) {
      if (!uuid[i]) {
        r = 0 | Math.random()*16;
        uuid[i] = chars[(i == 19) ? (r & 0x3) | 0x8 : r];
      }
    }
  }

  return uuid.join('');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.uri"></a>[module jake.uri](#apidoc.module.jake.uri)

#### <a name="apidoc.element.jake.uri.getFileExtension"></a>[function <span class="apidocSignatureSpan">jake.uri.</span>getFileExtension (path)](#apidoc.element.jake.uri.getFileExtension)
- description and source-code
```javascript
getFileExtension = function (path) {
  var match;
  if (path) {
    match = /.+\.(\w{2,4}$)/.exec(path);
  }
  return (match && match[1]) || '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.uri.objectify"></a>[function <span class="apidocSignatureSpan">jake.uri.</span>objectify (str, o)](#apidoc.element.jake.uri.objectify)
- description and source-code
```javascript
objectify = function (str, o) {
  var opts = o || {};
  var d = {};
  var consolidate = typeof opts.consolidate == 'undefined' ?
      true : opts.consolidate;
  if (str) {
    var arr = str.split('&');
    for (var i = 0; i < arr.length; i++) {
      var pair = arr[i].split('=');
      var name = pair[0];
      var val = decodeURIComponent(pair[1] || '');
      // "We've already got one!" -- arrayize if the flag
      // is set
      if (typeof d[name] != 'undefined' && consolidate) {
        if (typeof d[name] == 'string') {
          d[name] = [d[name]];
        }
        d[name].push(val);
      }
      // Otherwise just set the value
      else {
        d[name] = val;
      }
    }
  }
  return d;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jake.uri.paramify"></a>[function <span class="apidocSignatureSpan">jake.uri.</span>paramify (obj, o)](#apidoc.element.jake.uri.paramify)
- description and source-code
```javascript
paramify = function (obj, o) {
  var opts = o || {},
      _opts,
      str = '',
      key,
      val,
      isValid,
      itemArray,
      arr = [],
      arrVal,
      prefix = opts.prefix || '',
      self = this;

  function getParamName(key)
  {
    if (opts.prefix) {
      return prefix + '[' + key + ']';
    }
    else {
      return key;
    }
  }

  for (var p in obj) {
    if (Object.prototype.hasOwnProperty.call(obj, p)) {
      val = obj[p];

      // This keeps valid falsy values like false and 0
      // It's duplicated in the array block below. Could
      // put it in a function but don't want the overhead
      isValid = !( val === null || val === undefined ||
                  (typeof val === 'number' && isNaN(val)) );

      key = opts.snakeize ? string.snakeize(p) : p;
      if (isValid) {
        // Multiple vals -- array
        if (_isArray(val) && val.length) {
          itemArray = [];
          for (var i = 0, ii = val.length; i < ii; i++) {
            arrVal = val[i];
            // This keeps valid falsy values like false and 0
            isValid = !( arrVal === null || arrVal === undefined ||
                         (typeof arrVal === 'number' && isNaN(arrVal)) );

            // for index mode, which works recursive
            // objects and array must not be encoded
            if (opts.index && typeof arrVal === 'object') {
              itemArray[i] = arrVal;
            }
            else {
              itemArray[i] = isValid ? encodeURIComponent(arrVal) : '';

              if (opts.escapeVals) {
                itemArray[i] = string.escapeXML(itemArray[i]);
              }
            }
          }
          // Consolidation mode -- single value joined on comma
          if (opts.consolidate) {
            arr.push(getParamName(key) + '=' + itemArray.join(','));
          }
          // Indexed mode -- multiple, same-named params with numeric indices
          else if (opts.index) {
            // {foo: [1, 2, 3]} => 'foo[0]=1&foo[1]=2&foo[2]=3'

            itemArray.forEach(function(item, i) {
              // recursion of arrays
              if (_isArray(item) && item.length) {
                _opts = mixin(opts, {});
                item.forEach(function(_item, ii) {

                  if (typeof _item === 'object') {
                    _opts.prefix = getParamName(key) + '[' + i + '][' + ii + ']';
                    arr.push(self.paramify(_item, _opts));
                  }
                  else {
                    arr.push(getParamName(key) + '[' + i + '][' + ii + ']=' + _item);
                  }
                });
              }
              // recursion of object in array
              else if (typeof item === 'object') {
                _opts = mixin(opts, {});
                _opts.prefix = getParamName(key) + '[' + i + ']';
                arr.push(self.paramify(item, _opts));
              }
              // primitive
              else {
                arr.push(getParamName(key) + '[' + i + ']=' + item);
              }
            });
          }
          // Normal mode -- multiple, same-named params with each val
          else {
            // {foo: [1, 2, 3]} => 'foo=1&foo=2&foo=3'
            // Add into results array, as this just ends up getting
            // joined on ampersand at the end anyhow
            arr.push(getParamName(key) + '=' + itemArray.join('&' + getParamName(key) + '='));
          }
        }
        // Object -- recursion
        else if (typeof val === 'object') {
          _opts = mixin(opts, {});
          _opts.prefix = getParamName(key);

          arr.push(this.paramify(val, _opts));
        }
        // Single val -- string
        else {
          if (opts.escapeVals) {
            val = string.escapeXML(val);
          }
          arr.push(getParamName(key) + '=' + encodeURIComponent(val));
        }
        str += '&';
      }
      else {
        if (opts.includeEmpty) { arr.push(getParamName(key) + '='); }
      }
    }
  }
  return arr.join('&');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jake.watch_task"></a>[module jake.watch_task](#apidoc.module.jake.watch_task)

#### <a name="apidoc.element.jake.watch_task.WatchTask"></a>[function <span class="apidocSignatureSpan">jake.watch_task.</span>WatchTask ()](#apidoc.element.jake.watch_task.WatchTask)
- description and source-code
```javascript
WatchTask = function () {
  var self = this
    , args = Array.prototype.slice.call(arguments)
    , arg
    , definition
    , taskNames
    , name
    , last = (new Date()).getTime() - THROTTLE;

  args = args.filter(function (a) {
    return !!a;
  });

  while ((arg = args.shift())) {
    if (typeof arg == 'string') {
      name = arg;
    }
    else if (typeof arg == 'object' && Array.isArray(arg)) {
      taskNames = arg;
    }
    else if (typeof arg == 'function') {
      definition = arg;
    }
  }

  if (!(taskNames && taskNames.length)) {
    throw new Error('Watch task needs some tasks to run');
  }

  name = name || 'watch';
  definition = definition || function () {};

  if (jake.Task[name]) {
    throw new Error('WatchTask named "' + name + '" already exists. ' +
      'Please use a different name.');
  }

  this.watchTasks = Array.isArray(taskNames) ? taskNames : [taskNames];
  this.watchFiles = new FileList();
  this.rootTask = task('watchTasks', this.watchTasks);
  this.throttle = THROTTLE;

  this.watchFiles.include(WatchTask.DEFAULT_INCLUDE_FILES);
  this.watchFiles.exclude(WatchTask.DEFAULT_EXCLUDE_FILES);

  if (typeof definition == 'function') {
    definition.call(this);
  }

  desc('Runs these tasks: ' + this.watchTasks.join(', '));
  task(name, function () {
    console.log('WatchTask started for: ' + self.watchTasks.join(', '));
    jake.watch('.', {includePattern: /.+/}, function (filePath) {
      var fileMatch = self.watchFiles.toArray().some(function (item) {
        return item == filePath;
      });
      if (fileMatch && ((new Date()).getTime() - last) > self.throttle) {
        last = (new Date()).getTime();
        self.rootTask.reenable(true);
        self.rootTask.invoke();
      }
    });
  });
}
```
- example usage
```shell
...

// Backward-compat
this.npmPublishTask = function (name, prereqs, opts, definition) {
  return new jake.PublishTask(name, prereqs, opts, definition);
};

this.watchTask = function (name, taskNames, definition) {
  return new jake.WatchTask(name, taskNames, definition);
};

this.testTask = function () {
  var ctor = function () {}
    , t;
  ctor.prototype = jake.TestTask.prototype;
  t = new ctor();
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
