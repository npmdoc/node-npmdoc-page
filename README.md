# api documentation for  [page (v1.7.1)](https://github.com/visionmedia/page.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-page.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-page) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-page.svg)](https://travis-ci.org/npmdoc/node-npmdoc-page)
#### Tiny client-side router

[![NPM](https://nodei.co/npm/page.png?downloads=true)](https://www.npmjs.com/package/page)

[![apidoc](https://npmdoc.github.io/node-npmdoc-page/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-page_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-page/build/apidoc.html)

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
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "shuvalov-anton",
            "email": "anton_shuvalov@me.com"
        },
        {
            "name": "rstacruz",
            "email": "rico@ricostacruz.com"
        }
    ],
    "name": "page",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.7.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module page](#apidoc.module.page)
1.  [function <span class="apidocSignatureSpan"></span>page (path, fn)](#apidoc.element.page.page)
1.  [function <span class="apidocSignatureSpan">page.</span>Context (path, state)](#apidoc.element.page.Context)
1.  [function <span class="apidocSignatureSpan">page.</span>Route (path, options)](#apidoc.element.page.Route)
1.  [function <span class="apidocSignatureSpan">page.</span>back (path, state)](#apidoc.element.page.back)
1.  [function <span class="apidocSignatureSpan">page.</span>base (path)](#apidoc.element.page.base)
1.  [function <span class="apidocSignatureSpan">page.</span>dispatch (ctx)](#apidoc.element.page.dispatch)
1.  [function <span class="apidocSignatureSpan">page.</span>exit (path, fn)](#apidoc.element.page.exit)
1.  [function <span class="apidocSignatureSpan">page.</span>redirect (from, to)](#apidoc.element.page.redirect)
1.  [function <span class="apidocSignatureSpan">page.</span>replace (path, state, init, dispatch)](#apidoc.element.page.replace)
1.  [function <span class="apidocSignatureSpan">page.</span>sameOrigin (href)](#apidoc.element.page.sameOrigin)
1.  [function <span class="apidocSignatureSpan">page.</span>show (path, state, dispatch, push)](#apidoc.element.page.show)
1.  [function <span class="apidocSignatureSpan">page.</span>start (options)](#apidoc.element.page.start)
1.  [function <span class="apidocSignatureSpan">page.</span>stop ()](#apidoc.element.page.stop)
1.  number <span class="apidocSignatureSpan">page.</span>len
1.  object <span class="apidocSignatureSpan">page.</span>Context.prototype
1.  object <span class="apidocSignatureSpan">page.</span>Route.prototype
1.  object <span class="apidocSignatureSpan">page.</span>callbacks
1.  object <span class="apidocSignatureSpan">page.</span>exits
1.  string <span class="apidocSignatureSpan">page.</span>current

#### [module page.Context](#apidoc.module.page.Context)
1.  [function <span class="apidocSignatureSpan">page.</span>Context (path, state)](#apidoc.element.page.Context.Context)

#### [module page.Context.prototype](#apidoc.module.page.Context.prototype)
1.  [function <span class="apidocSignatureSpan">page.Context.prototype.</span>pushState ()](#apidoc.element.page.Context.prototype.pushState)
1.  [function <span class="apidocSignatureSpan">page.Context.prototype.</span>save ()](#apidoc.element.page.Context.prototype.save)

#### [module page.Route](#apidoc.module.page.Route)
1.  [function <span class="apidocSignatureSpan">page.</span>Route (path, options)](#apidoc.element.page.Route.Route)

#### [module page.Route.prototype](#apidoc.module.page.Route.prototype)
1.  [function <span class="apidocSignatureSpan">page.Route.prototype.</span>match (path, params)](#apidoc.element.page.Route.prototype.match)
1.  [function <span class="apidocSignatureSpan">page.Route.prototype.</span>middleware (fn)](#apidoc.element.page.Route.prototype.middleware)

#### [module page.page](#apidoc.module.page.page)
1.  [function <span class="apidocSignatureSpan">page.</span>page (path, fn)](#apidoc.element.page.page.page)
1.  [function <span class="apidocSignatureSpan">page.page.</span>Context (path, state)](#apidoc.element.page.page.Context)
1.  [function <span class="apidocSignatureSpan">page.page.</span>Route (path, options)](#apidoc.element.page.page.Route)
1.  [function <span class="apidocSignatureSpan">page.page.</span>back (path, state)](#apidoc.element.page.page.back)
1.  [function <span class="apidocSignatureSpan">page.page.</span>base (path)](#apidoc.element.page.page.base)
1.  [function <span class="apidocSignatureSpan">page.page.</span>dispatch (ctx)](#apidoc.element.page.page.dispatch)
1.  [function <span class="apidocSignatureSpan">page.page.</span>exit (path, fn)](#apidoc.element.page.page.exit)
1.  [function <span class="apidocSignatureSpan">page.page.</span>redirect (from, to)](#apidoc.element.page.page.redirect)
1.  [function <span class="apidocSignatureSpan">page.page.</span>replace (path, state, init, dispatch)](#apidoc.element.page.page.replace)
1.  [function <span class="apidocSignatureSpan">page.page.</span>sameOrigin (href)](#apidoc.element.page.page.sameOrigin)
1.  [function <span class="apidocSignatureSpan">page.page.</span>show (path, state, dispatch, push)](#apidoc.element.page.page.show)
1.  [function <span class="apidocSignatureSpan">page.page.</span>start (options)](#apidoc.element.page.page.start)
1.  [function <span class="apidocSignatureSpan">page.page.</span>stop ()](#apidoc.element.page.page.stop)
1.  number <span class="apidocSignatureSpan">page.page.</span>len
1.  object <span class="apidocSignatureSpan">page.page.</span>callbacks
1.  object <span class="apidocSignatureSpan">page.page.</span>exits
1.  string <span class="apidocSignatureSpan">page.page.</span>current



# <a name="apidoc.module.page"></a>[module page](#apidoc.module.page)

#### <a name="apidoc.element.page.page"></a>[function <span class="apidocSignatureSpan"></span>page (path, fn)](#apidoc.element.page.page)
- description and source-code
```javascript
function page(path, fn) {
  // <callback>
  if ('function' === typeof path) {
    return page('*', path);
  }

  // route <path> to <callback ...>
  if ('function' === typeof fn) {
    var route = new Route(/** @type {string} */ (path));
    for (var i = 1; i < arguments.length; ++i) {
      page.callbacks.push(route.middleware(arguments[i]));
    }
    // show <path> with [state]
  } else if ('string' === typeof path) {
    page['string' === typeof fn ? 'redirect' : 'show'](path, fn);
    // start [options]
  } else {
    page.start(path);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.Context"></a>[function <span class="apidocSignatureSpan">page.</span>Context (path, state)](#apidoc.element.page.Context)
- description and source-code
```javascript
function Context(path, state) {
  if ('/' === path[0] && 0 !== path.indexOf(base)) path = base + (hashbang ? '#!' : '') + path;
  var i = path.indexOf('?');

  this.canonicalPath = path;
  this.path = path.replace(base, '') || '/';
  if (hashbang) this.path = this.path.replace('#!', '') || '/';

  this.title = document.title;
  this.state = state || {};
  this.state.path = path;
  this.querystring = ~i ? decodeURLEncodedURIComponent(path.slice(i + 1)) : '';
  this.pathname = decodeURLEncodedURIComponent(~i ? path.slice(0, i) : path);
  this.params = {};

  // fragment
  this.hash = '';
  if (!hashbang) {
    if (!~this.path.indexOf('#')) return;
    var parts = this.path.split('#');
    this.path = parts[0];
    this.hash = decodeURLEncodedURIComponent(parts[1]) || '';
    this.querystring = this.querystring.split('#')[0];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.Route"></a>[function <span class="apidocSignatureSpan">page.</span>Route (path, options)](#apidoc.element.page.Route)
- description and source-code
```javascript
function Route(path, options) {
  options = options || {};
  this.path = (path === '*') ? '(.*)' : path;
  this.method = 'GET';
  this.regexp = pathtoRegexp(this.path,
    this.keys = [],
    options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.back"></a>[function <span class="apidocSignatureSpan">page.</span>back (path, state)](#apidoc.element.page.back)
- description and source-code
```javascript
back = function (path, state) {
  if (page.len > 0) {
    // this may need more testing to see if all browsers
    // wait for the next tick to go back in history
    history.back();
    page.len--;
  } else if (path) {
    setTimeout(function() {
      page.show(path, state);
    });
  }else{
    setTimeout(function() {
      page.show(base, state);
    });
  }
}
```
- example usage
```shell
...
 * @api public
 */

page.back = function(path, state) {
  if (page.len > 0) {
    // this may need more testing to see if all browsers
    // wait for the next tick to go back in history
    history.back();
    page.len--;
  } else if (path) {
    setTimeout(function() {
      page.show(path, state);
    });
  }else{
    setTimeout(function() {
...
```

#### <a name="apidoc.element.page.base"></a>[function <span class="apidocSignatureSpan">page.</span>base (path)](#apidoc.element.page.base)
- description and source-code
```javascript
base = function (path) {
  if (0 === arguments.length) return base;
  base = path;
}
```
- example usage
```shell
...

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

Get or set the base 'path'. For example if page.js
is operating within '/blog/*' set the base path to "/blog".

### page.exit(path, callback[, callback ...])

Defines an exit route mapping 'path' to the given 'callback(s)'.
...
```

#### <a name="apidoc.element.page.dispatch"></a>[function <span class="apidocSignatureSpan">page.</span>dispatch (ctx)](#apidoc.element.page.dispatch)
- description and source-code
```javascript
dispatch = function (ctx) {
  var prev = prevContext,
    i = 0,
    j = 0;

  prevContext = ctx;

  function nextExit() {
    var fn = page.exits[j++];
    if (!fn) return nextEnter();
    fn(prev, nextExit);
  }

  function nextEnter() {
    var fn = page.callbacks[i++];

    if (ctx.path !== page.current) {
      ctx.handled = false;
      return;
    }
    if (!fn) return unhandled(ctx);
    fn(ctx, nextEnter);
  }

  if (prev) {
    nextExit();
  } else {
    nextEnter();
  }
}
```
- example usage
```shell
...
 * @return {!Context}
 * @api public
 */

page.show = function(path, state, dispatch, push) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  if (false !== dispatch) page.dispatch(ctx);
  if (false !== ctx.handled && false !== push) ctx.pushState();
  return ctx;
};

/**
 * Goes back in the history
 * Back should always let the current route push state and then go back.
...
```

#### <a name="apidoc.element.page.exit"></a>[function <span class="apidocSignatureSpan">page.</span>exit (path, fn)](#apidoc.element.page.exit)
- description and source-code
```javascript
exit = function (path, fn) {
  if (typeof path === 'function') {
    return page.exit('*', path);
  }

  var route = new Route(path);
  for (var i = 1; i < arguments.length; ++i) {
    page.exits.push(route.middleware(arguments[i]));
  }
}
```
- example usage
```shell
...
  Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

  Get or set the base 'path'. For example if page.js
  is operating within '/blog/*' set the base path to "/blog".

### page.exit(path, callback[, callback ...])

  Defines an exit route mapping 'path' to the given 'callback(s)'.

  Exit routes are called when a page changes, using the context
  from the previous change. For example:

'''js
...
```

#### <a name="apidoc.element.page.redirect"></a>[function <span class="apidocSignatureSpan">page.</span>redirect (from, to)](#apidoc.element.page.redirect)
- description and source-code
```javascript
redirect = function (from, to) {
  // Define route from a path to another
  if ('string' === typeof from && 'string' === typeof to) {
    page(from, function(e) {
      setTimeout(function() {
        page.replace(/** @type {!string} */ (to));
      }, 0);
    });
  }

  // Wait for the push state and replace it with another
  if ('string' === typeof from && 'undefined' === typeof to) {
    setTimeout(function() {
      page.replace(from);
    }, 0);
  }
}
```
- example usage
```shell
...
})
'''

### page(fromPath, toPath)

Setup redirect from one path to another.

### page.redirect(fromPath, toPath)

Identical to 'page(fromPath, toPath)'

### page.redirect(path)
Calling page.redirect with only a string as the first parameter
redirects to another route.
Waits for the current route to push state and after replaces it
...
```

#### <a name="apidoc.element.page.replace"></a>[function <span class="apidocSignatureSpan">page.</span>replace (path, state, init, dispatch)](#apidoc.element.page.replace)
- description and source-code
```javascript
replace = function (path, state, init, dispatch) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  ctx.init = init;
  ctx.save(); // save before dispatching, which may redirect
  if (false !== dispatch) page.dispatch(ctx);
  return ctx;
}
```
- example usage
```shell
...
  if (false !== options.popstate) window.addEventListener('popstate', onpopstate, false);
  if (false !== options.click) {
    document.addEventListener(clickEvent, onclick, false);
  }
  if (true === options.hashbang) hashbang = true;
  if (!dispatch) return;
  var url = (hashbang && ~location.hash.indexOf('#!')) ? location.hash.substr(2) + location.search : location.pathname + location
.search + location.hash;
  page.replace(url, null, true, dispatch);
};

/**
 * Unbind click and popstate event handlers.
 *
 * @api public
 */
...
```

#### <a name="apidoc.element.page.sameOrigin"></a>[function <span class="apidocSignatureSpan">page.</span>sameOrigin (href)](#apidoc.element.page.sameOrigin)
- description and source-code
```javascript
function sameOrigin(href) {
  var origin = location.protocol + '//' + location.hostname;
  if (location.port) origin += ':' + location.port;
  return (href && (0 === href.indexOf(origin)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.show"></a>[function <span class="apidocSignatureSpan">page.</span>show (path, state, dispatch, push)](#apidoc.element.page.show)
- description and source-code
```javascript
show = function (path, state, dispatch, push) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  if (false !== dispatch) page.dispatch(ctx);
  if (false !== ctx.handled && false !== push) ctx.pushState();
  return ctx;
}
```
- example usage
```shell
...
  page.redirect('/guest');
}
});

page('/default');
'''

### page.show(path)

Identical to 'page(path)' above.

### page([options])

Register page's 'popstate' / 'click' bindings. If you're
doing selective binding you'll like want to pass '{ click: false }'
...
```

#### <a name="apidoc.element.page.start"></a>[function <span class="apidocSignatureSpan">page.</span>start (options)](#apidoc.element.page.start)
- description and source-code
```javascript
start = function (options) {
  options = options || {};
  if (running) return;
  running = true;
  if (false === options.dispatch) dispatch = false;
  if (false === options.decodeURLComponents) decodeURLComponents = false;
  if (false !== options.popstate) window.addEventListener('popstate', onpopstate, false);
  if (false !== options.click) {
    document.addEventListener(clickEvent, onclick, false);
  }
  if (true === options.hashbang) hashbang = true;
  if (!dispatch) return;
  var url = (hashbang && ~location.hash.indexOf('#!')) ? location.hash.substr(2) + location.search : location.pathname + location
.search + location.hash;
  page.replace(url, null, true, dispatch);
}
```
- example usage
```shell
...
- 'hashbang' add '#!' before urls [__false__]
- 'decodeURLComponents' remove URL encoding from path components (query string, pathname, hash) [__true__]

If you wish to load serve initial content
from the server you likely will want to
set 'dispatch' to __false__.

### page.start([options])

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.
...
```

#### <a name="apidoc.element.page.stop"></a>[function <span class="apidocSignatureSpan">page.</span>stop ()](#apidoc.element.page.stop)
- description and source-code
```javascript
stop = function () {
  if (!running) return;
  page.current = '';
  page.len = 0;
  running = false;
  document.removeEventListener(clickEvent, onclick, false);
  window.removeEventListener('popstate', onpopstate, false);
}
```
- example usage
```shell
...
from the server you likely will want to
set 'dispatch' to __false__.

### page.start([options])

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

Get or set the base 'path'. For example if page.js
is operating within '/blog/*' set the base path to "/blog".
...
```



# <a name="apidoc.module.page.Context"></a>[module page.Context](#apidoc.module.page.Context)

#### <a name="apidoc.element.page.Context.Context"></a>[function <span class="apidocSignatureSpan">page.</span>Context (path, state)](#apidoc.element.page.Context.Context)
- description and source-code
```javascript
function Context(path, state) {
  if ('/' === path[0] && 0 !== path.indexOf(base)) path = base + (hashbang ? '#!' : '') + path;
  var i = path.indexOf('?');

  this.canonicalPath = path;
  this.path = path.replace(base, '') || '/';
  if (hashbang) this.path = this.path.replace('#!', '') || '/';

  this.title = document.title;
  this.state = state || {};
  this.state.path = path;
  this.querystring = ~i ? decodeURLEncodedURIComponent(path.slice(i + 1)) : '';
  this.pathname = decodeURLEncodedURIComponent(~i ? path.slice(0, i) : path);
  this.params = {};

  // fragment
  this.hash = '';
  if (!hashbang) {
    if (!~this.path.indexOf('#')) return;
    var parts = this.path.split('#');
    this.path = parts[0];
    this.hash = decodeURLEncodedURIComponent(parts[1]) || '';
    this.querystring = this.querystring.split('#')[0];
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.page.Context.prototype"></a>[module page.Context.prototype](#apidoc.module.page.Context.prototype)

#### <a name="apidoc.element.page.Context.prototype.pushState"></a>[function <span class="apidocSignatureSpan">page.Context.prototype.</span>pushState ()](#apidoc.element.page.Context.prototype.pushState)
- description and source-code
```javascript
pushState = function () {
  page.len++;
  history.pushState(this.state, this.title, hashbang && this.path !== '/' ? '#!' + this.path : this.canonicalPath);
}
```
- example usage
```shell
...
 * @api public
 */

page.show = function(path, state, dispatch, push) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  if (false !== dispatch) page.dispatch(ctx);
  if (false !== ctx.handled && false !== push) ctx.pushState();
  return ctx;
};

/**
 * Goes back in the history
 * Back should always let the current route push state and then go back.
 *
...
```

#### <a name="apidoc.element.page.Context.prototype.save"></a>[function <span class="apidocSignatureSpan">page.Context.prototype.</span>save ()](#apidoc.element.page.Context.prototype.save)
- description and source-code
```javascript
save = function () {
  history.replaceState(this.state, this.title, hashbang && this.path !== '/' ? '#!' + this.path : this.canonicalPath);
}
```
- example usage
```shell
...
'''js
function show(ctx){
if (ctx.state.images) {
  displayImages(ctx.state.images)
} else {
  $.getJSON('/photos', function(images){
    ctx.state.images = images
    ctx.save()
    displayImages(images)
  })
}
}
'''

__NOTE__: 'ctx.save()' must be used
...
```



# <a name="apidoc.module.page.Route"></a>[module page.Route](#apidoc.module.page.Route)

#### <a name="apidoc.element.page.Route.Route"></a>[function <span class="apidocSignatureSpan">page.</span>Route (path, options)](#apidoc.element.page.Route.Route)
- description and source-code
```javascript
function Route(path, options) {
  options = options || {};
  this.path = (path === '*') ? '(.*)' : path;
  this.method = 'GET';
  this.regexp = pathtoRegexp(this.path,
    this.keys = [],
    options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.page.Route.prototype"></a>[module page.Route.prototype](#apidoc.module.page.Route.prototype)

#### <a name="apidoc.element.page.Route.prototype.match"></a>[function <span class="apidocSignatureSpan">page.Route.prototype.</span>match (path, params)](#apidoc.element.page.Route.prototype.match)
- description and source-code
```javascript
match = function (path, params) {
  var keys = this.keys,
    qsIndex = path.indexOf('?'),
    pathname = ~qsIndex ? path.slice(0, qsIndex) : path,
    m = this.regexp.exec(decodeURIComponent(pathname));

  if (!m) return false;

  for (var i = 1, len = m.length; i < len; ++i) {
    var key = keys[i - 1];
    var val = decodeURLEncodedURIComponent(m[i]);
    if (val !== undefined || !(hasOwnProperty.call(params, key.name))) {
      params[key.name] = val;
    }
  }

  return true;
}
```
- example usage
```shell
...
 * @return {Function}
 * @api public
 */

Route.prototype.middleware = function(fn) {
  var self = this;
  return function(ctx, next) {
    if (self.match(ctx.path, ctx.params)) return fn(ctx, next);
    next();
  };
};

/**
 * Check if this route matches 'path', if so
 * populate 'params'.
...
```

#### <a name="apidoc.element.page.Route.prototype.middleware"></a>[function <span class="apidocSignatureSpan">page.Route.prototype.</span>middleware (fn)](#apidoc.element.page.Route.prototype.middleware)
- description and source-code
```javascript
middleware = function (fn) {
  var self = this;
  return function(ctx, next) {
    if (self.match(ctx.path, ctx.params)) return fn(ctx, next);
    next();
  };
}
```
- example usage
```shell
...
  return page('*', path);
}

// route <path> to <callback ...>
if ('function' === typeof fn) {
  var route = new Route(/** @type {string} */ (path));
  for (var i = 1; i < arguments.length; ++i) {
    page.callbacks.push(route.middleware(arguments[i]));
  }
  // show <path> with [state]
} else if ('string' === typeof path) {
  page['string' === typeof fn ? 'redirect' : 'show'](path, fn);
  // start [options]
} else {
  page.start(path);
...
```



# <a name="apidoc.module.page.page"></a>[module page.page](#apidoc.module.page.page)

#### <a name="apidoc.element.page.page.page"></a>[function <span class="apidocSignatureSpan">page.</span>page (path, fn)](#apidoc.element.page.page.page)
- description and source-code
```javascript
function page(path, fn) {
  // <callback>
  if ('function' === typeof path) {
    return page('*', path);
  }

  // route <path> to <callback ...>
  if ('function' === typeof fn) {
    var route = new Route(/** @type {string} */ (path));
    for (var i = 1; i < arguments.length; ++i) {
      page.callbacks.push(route.middleware(arguments[i]));
    }
    // show <path> with [state]
  } else if ('string' === typeof path) {
    page['string' === typeof fn ? 'redirect' : 'show'](path, fn);
    // start [options]
  } else {
    page.start(path);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.page.Context"></a>[function <span class="apidocSignatureSpan">page.page.</span>Context (path, state)](#apidoc.element.page.page.Context)
- description and source-code
```javascript
function Context(path, state) {
  if ('/' === path[0] && 0 !== path.indexOf(base)) path = base + (hashbang ? '#!' : '') + path;
  var i = path.indexOf('?');

  this.canonicalPath = path;
  this.path = path.replace(base, '') || '/';
  if (hashbang) this.path = this.path.replace('#!', '') || '/';

  this.title = document.title;
  this.state = state || {};
  this.state.path = path;
  this.querystring = ~i ? decodeURLEncodedURIComponent(path.slice(i + 1)) : '';
  this.pathname = decodeURLEncodedURIComponent(~i ? path.slice(0, i) : path);
  this.params = {};

  // fragment
  this.hash = '';
  if (!hashbang) {
    if (!~this.path.indexOf('#')) return;
    var parts = this.path.split('#');
    this.path = parts[0];
    this.hash = decodeURLEncodedURIComponent(parts[1]) || '';
    this.querystring = this.querystring.split('#')[0];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.page.Route"></a>[function <span class="apidocSignatureSpan">page.page.</span>Route (path, options)](#apidoc.element.page.page.Route)
- description and source-code
```javascript
function Route(path, options) {
  options = options || {};
  this.path = (path === '*') ? '(.*)' : path;
  this.method = 'GET';
  this.regexp = pathtoRegexp(this.path,
    this.keys = [],
    options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.page.back"></a>[function <span class="apidocSignatureSpan">page.page.</span>back (path, state)](#apidoc.element.page.page.back)
- description and source-code
```javascript
back = function (path, state) {
  if (page.len > 0) {
    // this may need more testing to see if all browsers
    // wait for the next tick to go back in history
    history.back();
    page.len--;
  } else if (path) {
    setTimeout(function() {
      page.show(path, state);
    });
  }else{
    setTimeout(function() {
      page.show(base, state);
    });
  }
}
```
- example usage
```shell
...
 * @api public
 */

page.back = function(path, state) {
  if (page.len > 0) {
    // this may need more testing to see if all browsers
    // wait for the next tick to go back in history
    history.back();
    page.len--;
  } else if (path) {
    setTimeout(function() {
      page.show(path, state);
    });
  }else{
    setTimeout(function() {
...
```

#### <a name="apidoc.element.page.page.base"></a>[function <span class="apidocSignatureSpan">page.page.</span>base (path)](#apidoc.element.page.page.base)
- description and source-code
```javascript
base = function (path) {
  if (0 === arguments.length) return base;
  base = path;
}
```
- example usage
```shell
...

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

Get or set the base 'path'. For example if page.js
is operating within '/blog/*' set the base path to "/blog".

### page.exit(path, callback[, callback ...])

Defines an exit route mapping 'path' to the given 'callback(s)'.
...
```

#### <a name="apidoc.element.page.page.dispatch"></a>[function <span class="apidocSignatureSpan">page.page.</span>dispatch (ctx)](#apidoc.element.page.page.dispatch)
- description and source-code
```javascript
dispatch = function (ctx) {
  var prev = prevContext,
    i = 0,
    j = 0;

  prevContext = ctx;

  function nextExit() {
    var fn = page.exits[j++];
    if (!fn) return nextEnter();
    fn(prev, nextExit);
  }

  function nextEnter() {
    var fn = page.callbacks[i++];

    if (ctx.path !== page.current) {
      ctx.handled = false;
      return;
    }
    if (!fn) return unhandled(ctx);
    fn(ctx, nextEnter);
  }

  if (prev) {
    nextExit();
  } else {
    nextEnter();
  }
}
```
- example usage
```shell
...
 * @return {!Context}
 * @api public
 */

page.show = function(path, state, dispatch, push) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  if (false !== dispatch) page.dispatch(ctx);
  if (false !== ctx.handled && false !== push) ctx.pushState();
  return ctx;
};

/**
 * Goes back in the history
 * Back should always let the current route push state and then go back.
...
```

#### <a name="apidoc.element.page.page.exit"></a>[function <span class="apidocSignatureSpan">page.page.</span>exit (path, fn)](#apidoc.element.page.page.exit)
- description and source-code
```javascript
exit = function (path, fn) {
  if (typeof path === 'function') {
    return page.exit('*', path);
  }

  var route = new Route(path);
  for (var i = 1; i < arguments.length; ++i) {
    page.exits.push(route.middleware(arguments[i]));
  }
}
```
- example usage
```shell
...
  Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

  Get or set the base 'path'. For example if page.js
  is operating within '/blog/*' set the base path to "/blog".

### page.exit(path, callback[, callback ...])

  Defines an exit route mapping 'path' to the given 'callback(s)'.

  Exit routes are called when a page changes, using the context
  from the previous change. For example:

'''js
...
```

#### <a name="apidoc.element.page.page.redirect"></a>[function <span class="apidocSignatureSpan">page.page.</span>redirect (from, to)](#apidoc.element.page.page.redirect)
- description and source-code
```javascript
redirect = function (from, to) {
  // Define route from a path to another
  if ('string' === typeof from && 'string' === typeof to) {
    page(from, function(e) {
      setTimeout(function() {
        page.replace(/** @type {!string} */ (to));
      }, 0);
    });
  }

  // Wait for the push state and replace it with another
  if ('string' === typeof from && 'undefined' === typeof to) {
    setTimeout(function() {
      page.replace(from);
    }, 0);
  }
}
```
- example usage
```shell
...
})
'''

### page(fromPath, toPath)

Setup redirect from one path to another.

### page.redirect(fromPath, toPath)

Identical to 'page(fromPath, toPath)'

### page.redirect(path)
Calling page.redirect with only a string as the first parameter
redirects to another route.
Waits for the current route to push state and after replaces it
...
```

#### <a name="apidoc.element.page.page.replace"></a>[function <span class="apidocSignatureSpan">page.page.</span>replace (path, state, init, dispatch)](#apidoc.element.page.page.replace)
- description and source-code
```javascript
replace = function (path, state, init, dispatch) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  ctx.init = init;
  ctx.save(); // save before dispatching, which may redirect
  if (false !== dispatch) page.dispatch(ctx);
  return ctx;
}
```
- example usage
```shell
...
  if (false !== options.popstate) window.addEventListener('popstate', onpopstate, false);
  if (false !== options.click) {
    document.addEventListener(clickEvent, onclick, false);
  }
  if (true === options.hashbang) hashbang = true;
  if (!dispatch) return;
  var url = (hashbang && ~location.hash.indexOf('#!')) ? location.hash.substr(2) + location.search : location.pathname + location
.search + location.hash;
  page.replace(url, null, true, dispatch);
};

/**
 * Unbind click and popstate event handlers.
 *
 * @api public
 */
...
```

#### <a name="apidoc.element.page.page.sameOrigin"></a>[function <span class="apidocSignatureSpan">page.page.</span>sameOrigin (href)](#apidoc.element.page.page.sameOrigin)
- description and source-code
```javascript
function sameOrigin(href) {
  var origin = location.protocol + '//' + location.hostname;
  if (location.port) origin += ':' + location.port;
  return (href && (0 === href.indexOf(origin)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.page.page.show"></a>[function <span class="apidocSignatureSpan">page.page.</span>show (path, state, dispatch, push)](#apidoc.element.page.page.show)
- description and source-code
```javascript
show = function (path, state, dispatch, push) {
  var ctx = new Context(path, state);
  page.current = ctx.path;
  if (false !== dispatch) page.dispatch(ctx);
  if (false !== ctx.handled && false !== push) ctx.pushState();
  return ctx;
}
```
- example usage
```shell
...
  page.redirect('/guest');
}
});

page('/default');
'''

### page.show(path)

Identical to 'page(path)' above.

### page([options])

Register page's 'popstate' / 'click' bindings. If you're
doing selective binding you'll like want to pass '{ click: false }'
...
```

#### <a name="apidoc.element.page.page.start"></a>[function <span class="apidocSignatureSpan">page.page.</span>start (options)](#apidoc.element.page.page.start)
- description and source-code
```javascript
start = function (options) {
  options = options || {};
  if (running) return;
  running = true;
  if (false === options.dispatch) dispatch = false;
  if (false === options.decodeURLComponents) decodeURLComponents = false;
  if (false !== options.popstate) window.addEventListener('popstate', onpopstate, false);
  if (false !== options.click) {
    document.addEventListener(clickEvent, onclick, false);
  }
  if (true === options.hashbang) hashbang = true;
  if (!dispatch) return;
  var url = (hashbang && ~location.hash.indexOf('#!')) ? location.hash.substr(2) + location.search : location.pathname + location
.search + location.hash;
  page.replace(url, null, true, dispatch);
}
```
- example usage
```shell
...
- 'hashbang' add '#!' before urls [__false__]
- 'decodeURLComponents' remove URL encoding from path components (query string, pathname, hash) [__true__]

If you wish to load serve initial content
from the server you likely will want to
set 'dispatch' to __false__.

### page.start([options])

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.
...
```

#### <a name="apidoc.element.page.page.stop"></a>[function <span class="apidocSignatureSpan">page.page.</span>stop ()](#apidoc.element.page.page.stop)
- description and source-code
```javascript
stop = function () {
  if (!running) return;
  page.current = '';
  page.len = 0;
  running = false;
  document.removeEventListener(clickEvent, onclick, false);
  window.removeEventListener('popstate', onpopstate, false);
}
```
- example usage
```shell
...
from the server you likely will want to
set 'dispatch' to __false__.

### page.start([options])

Identical to 'page([options])' above.

### page.stop()

Unbind both the 'popstate' and 'click' handlers.

### page.base([path])

Get or set the base 'path'. For example if page.js
is operating within '/blog/*' set the base path to "/blog".
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
