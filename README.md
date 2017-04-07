# api documentation for  [package (v1.0.1)](http://github.com/vesln/package)  [![npm package](https://img.shields.io/npm/v/npmdoc-package.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-package) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-package.svg)](https://travis-ci.org/npmdoc/node-npmdoc-package)
#### Easy package.json exports.

[![NPM](https://nodei.co/npm/package.png?downloads=true)](https://www.npmjs.com/package/package)

[![apidoc](https://npmdoc.github.io/node-npmdoc-package/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-package_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-package/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-package/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-package/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Veselin Todorov",
        "email": "hi@vesln.com"
    },
    "bugs": {
        "url": "https://github.com/vesln/package/issues"
    },
    "dependencies": {},
    "description": "Easy package.json exports.",
    "devDependencies": {
        "mocha": "0.3.3",
        "should": "0.3.2"
    },
    "directories": {},
    "dist": {
        "shasum": "d25a1f99e2506dcb27d6704b83dca8a312e4edcc",
        "tarball": "https://registry.npmjs.org/package/-/package-1.0.1.tgz"
    },
    "engines": {
        "node": ">= 0.6.0"
    },
    "homepage": "http://github.com/vesln/package",
    "keywords": [
        "package.json"
    ],
    "main": "./lib/package",
    "maintainers": [
        {
            "name": "vesln",
            "email": "hi@vesln.com"
        }
    ],
    "name": "package",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/vesln/package.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "1.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module package](#apidoc.module.package)
1.  [function <span class="apidocSignatureSpan">package.</span>discover (module)](#apidoc.element.package.discover)
1.  [function <span class="apidocSignatureSpan">package.</span>read (file)](#apidoc.element.package.read)



# <a name="apidoc.module.package"></a>[module package](#apidoc.module.package)

#### <a name="apidoc.element.package.discover"></a>[function <span class="apidocSignatureSpan">package.</span>discover (module)](#apidoc.element.package.discover)
- description and source-code
```javascript
discover = function (module) {
  var location = path.dirname(module.filename);
  var found = null;

  while (!found) {
    if (exists(location + '/package.json')) {
      found = location;
    } else if (location !== '/') {
      location = path.dirname(location);
    } else {
      throw new Error('package.json can not be located');
    }
  }

  return found;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.package.read"></a>[function <span class="apidocSignatureSpan">package.</span>read (file)](#apidoc.element.package.read)
- description and source-code
```javascript
read = function (file) {
  var data = fs.readFileSync(file, 'utf8');
  return JSON.parse(data);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
