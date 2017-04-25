# npmdoc-page

#### basic api documentation for  [page (v1.7.1)](https://github.com/visionmedia/page.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-page.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-page) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-page.svg)](https://travis-ci.org/npmdoc/node-npmdoc-page)

#### Tiny client-side router

[![NPM](https://nodei.co/npm/page.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/page)

- [https://npmdoc.github.io/node-npmdoc-page/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-page/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-page/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-page/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-page/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-page/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/visionmedia/page.js/issues"
    },
    "component": {
        "scripts": {
            "page": "index.js"
        }
    },
    "dependencies": {
        "path-to-regexp": "~1.2.1"
    },
    "description": "Tiny client-side router",
    "devDependencies": {
        "browserify": "^6.3.2",
        "chai": "^1.10.0",
        "coveralls": "^2.11.2",
        "express": "^4.10.2",
        "jade": "^1.7.0",
        "jscoverage": "^0.5.9",
        "jsdom": "^1.3.1",
        "jshint": "^2.5.10",
        "mocha": "^2.0.1",
        "mocha-lcov-reporter": "0.0.1",
        "serve": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "3886c147b895487783759b37e800a11213bc38ed",
        "tarball": "https://registry.npmjs.org/page/-/page-1.7.1.tgz"
    },
    "files": [
        "index.js",
        "page.js"
    ],
    "gitHead": "29884fb640f3bd4984b2a4a24aa3687b2f2221f7",
    "homepage": "https://github.com/visionmedia/page.js#readme",
    "license": "MIT",
    "maintainers": [
        {
            "name": "tjholowaychuk"
        },
        {
            "name": "shuvalov-anton"
        },
        {
            "name": "rstacruz"
        }
    ],
    "name": "page",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/visionmedia/page.js.git"
    },
    "scripts": {
        "make": "browserify index.js --standalone page -o page.js",
        "prepublish": "npm run make",
        "serve": "serve test",
        "test": "jshint index.js test/tests.js && mocha test/tests.js",
        "test-cov": "jscoverage index.js index-cov.js; PAGE_COV=1 mocha test/tests.js -R html-cov > coverage.html"
    },
    "version": "1.7.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
