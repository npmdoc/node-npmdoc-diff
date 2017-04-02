# api documentation for  [diff (v3.2.0)](https://github.com/kpdecker/jsdiff#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-diff.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-diff) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-diff.svg)](https://travis-ci.org/npmdoc/node-npmdoc-diff)
#### A javascript text diff implementation.

[![NPM](https://nodei.co/npm/diff.png?downloads=true)](https://www.npmjs.com/package/diff)

[![apidoc](https://npmdoc.github.io/node-npmdoc-diff/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-diff_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-diff/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-diff/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "babel": {
        "sourceMaps": "inline",
        "presets": [
            "es3",
            "es2015-mod"
        ],
        "auxiliaryCommentBefore": "istanbul ignore start",
        "auxiliaryCommentAfter": "istanbul ignore end"
    },
    "bugs": {
        "url": "http://github.com/kpdecker/jsdiff/issues",
        "email": "kpdecker@gmail.com"
    },
    "dependencies": {},
    "description": "A javascript text diff implementation.",
    "devDependencies": {
        "async": "^1.4.2",
        "babel-core": "^6.0.0",
        "babel-loader": "^6.0.0",
        "babel-preset-es2015-mod": "^6.3.13",
        "babel-preset-es3": "^1.0.1",
        "chai": "^3.3.0",
        "colors": "^1.1.2",
        "eslint": "^1.6.0",
        "grunt": "^0.4.5",
        "grunt-babel": "^6.0.0",
        "grunt-clean": "^0.4.0",
        "grunt-cli": "^0.1.13",
        "grunt-contrib-clean": "^1.0.0",
        "grunt-contrib-copy": "^1.0.0",
        "grunt-contrib-uglify": "^1.0.0",
        "grunt-contrib-watch": "^1.0.0",
        "grunt-eslint": "^17.3.1",
        "grunt-karma": "^0.12.1",
        "grunt-mocha-istanbul": "^3.0.1",
        "grunt-mocha-test": "^0.12.7",
        "grunt-webpack": "^1.0.11",
        "istanbul": "github:kpdecker/istanbul",
        "karma": "^0.13.11",
        "karma-mocha": "^0.2.0",
        "karma-mocha-reporter": "^2.0.0",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-sauce-launcher": "^0.3.0",
        "karma-sourcemap-loader": "^0.3.6",
        "karma-webpack": "^1.7.0",
        "mocha": "^2.3.3",
        "phantomjs-prebuilt": "^2.1.5",
        "semver": "^5.0.3",
        "webpack": "^1.12.2",
        "webpack-dev-server": "^1.12.0"
    },
    "directories": {},
    "dist": {
        "shasum": "c9ce393a4b7cbd0b058a725c93df299027868ff9",
        "tarball": "https://registry.npmjs.org/diff/-/diff-3.2.0.tgz"
    },
    "engines": {
        "node": ">=0.3.1"
    },
    "gitHead": "becde77e9f7aa31944480cf2a335815cd44d2d12",
    "homepage": "https://github.com/kpdecker/jsdiff#readme",
    "keywords": [
        "diff",
        "javascript"
    ],
    "license": "BSD-3-Clause",
    "main": "./lib",
    "maintainers": [
        {
            "name": "kpdecker",
            "email": "kpdecker@gmail.com"
        }
    ],
    "name": "diff",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/kpdecker/jsdiff.git"
    },
    "scripts": {
        "test": "grunt"
    },
    "version": "3.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module diff](#apidoc.module.diff)
1.  boolean <span class="apidocSignatureSpan">diff.</span>__esModule
1.  [function <span class="apidocSignatureSpan">diff.</span>Diff ()](#apidoc.element.diff.Diff)
1.  [function <span class="apidocSignatureSpan">diff.</span>applyPatch (source, uniDiff)](#apidoc.element.diff.applyPatch)
1.  [function <span class="apidocSignatureSpan">diff.</span>applyPatches (uniDiff, options)](#apidoc.element.diff.applyPatches)
1.  [function <span class="apidocSignatureSpan">diff.</span>canonicalize (obj, stack, replacementStack)](#apidoc.element.diff.canonicalize)
1.  [function <span class="apidocSignatureSpan">diff.</span>convertChangesToDMP (changes)](#apidoc.element.diff.convertChangesToDMP)
1.  [function <span class="apidocSignatureSpan">diff.</span>convertChangesToXML (changes)](#apidoc.element.diff.convertChangesToXML)
1.  [function <span class="apidocSignatureSpan">diff.</span>createPatch (fileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.createPatch)
1.  [function <span class="apidocSignatureSpan">diff.</span>createTwoFilesPatch (oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.createTwoFilesPatch)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffArrays (oldArr, newArr, callback)](#apidoc.element.diff.diffArrays)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffChars (oldStr, newStr, callback)](#apidoc.element.diff.diffChars)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffCss (oldStr, newStr, callback)](#apidoc.element.diff.diffCss)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffJson (oldObj, newObj, options)](#apidoc.element.diff.diffJson)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffLines (oldStr, newStr, callback)](#apidoc.element.diff.diffLines)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffSentences (oldStr, newStr, callback)](#apidoc.element.diff.diffSentences)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffTrimmedLines (oldStr, newStr, callback)](#apidoc.element.diff.diffTrimmedLines)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffWords (oldStr, newStr, callback)](#apidoc.element.diff.diffWords)
1.  [function <span class="apidocSignatureSpan">diff.</span>diffWordsWithSpace (oldStr, newStr, callback)](#apidoc.element.diff.diffWordsWithSpace)
1.  [function <span class="apidocSignatureSpan">diff.</span>parsePatch (uniDiff)](#apidoc.element.diff.parsePatch)
1.  [function <span class="apidocSignatureSpan">diff.</span>structuredPatch (oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.structuredPatch)
1.  object <span class="apidocSignatureSpan">diff.</span>Diff.prototype

#### [module diff.Diff](#apidoc.module.diff.Diff)
1.  [function <span class="apidocSignatureSpan">diff.</span>Diff ()](#apidoc.element.diff.Diff.Diff)

#### [module diff.Diff.prototype](#apidoc.module.diff.Diff.prototype)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>castInput (value)](#apidoc.element.diff.Diff.prototype.castInput)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>diff (oldString, newString)](#apidoc.element.diff.Diff.prototype.diff)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>equals (left, right)](#apidoc.element.diff.Diff.prototype.equals)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>extractCommon (basePath, newString, oldString, diagonalPath)](#apidoc.element.diff.Diff.prototype.extractCommon)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>join (chars)](#apidoc.element.diff.Diff.prototype.join)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>pushComponent (components, added, removed)](#apidoc.element.diff.Diff.prototype.pushComponent)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>removeEmpty (array)](#apidoc.element.diff.Diff.prototype.removeEmpty)
1.  [function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>tokenize (value)](#apidoc.element.diff.Diff.prototype.tokenize)



# <a name="apidoc.module.diff"></a>[module diff](#apidoc.module.diff)

#### <a name="apidoc.element.diff.Diff"></a>[function <span class="apidocSignatureSpan">diff.</span>Diff ()](#apidoc.element.diff.Diff)
- description and source-code
```javascript
function Diff() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.applyPatch"></a>[function <span class="apidocSignatureSpan">diff.</span>applyPatch (source, uniDiff)](#apidoc.element.diff.applyPatch)
- description and source-code
```javascript
function applyPatch(source, uniDiff) {
<span class="apidocCodeCommentSpan">  /*istanbul ignore start*/var /*istanbul ignore end*/options = arguments.length <= 2 || arguments[2] === undefined ? {} : arguments
[2];

  if (typeof uniDiff === 'string') {
    uniDiff = /*istanbul ignore start*/(0, _parse.parsePatch) /*istanbul ignore end*/(uniDiff);
  }

  if (Array.isArray(uniDiff)) {
    if (uniDiff.length > 1) {
      throw new Error('applyPatch only works with a single input.');
    }

    uniDiff = uniDiff[0];
  }

  // Apply the diff to the input
  var lines = source.split(/\r\n|[\n\v\f\r\x85]/),
      delimiters = source.match(/\r\n|[\n\v\f\r\x85]/g) || [],
      hunks = uniDiff.hunks,
      compareLine = options.compareLine || function (lineNumber, line, operation, patchContent) /*istanbul ignore start*/{
    return (/*istanbul ignore end*/line === patchContent
    );
  },
      errorCount = 0,
      fuzzFactor = options.fuzzFactor || 0,
      minLine = 0,
      offset = 0,
      removeEOFNL = /*istanbul ignore start*/void 0 /*istanbul ignore end*/,
      addEOFNL = /*istanbul ignore start*/void 0 /*istanbul ignore end*/;

  /**
   * Checks if the hunk exactly fits on the provided location
   */
</span>  function hunkFits(hunk, toPos) {
    for (var j = 0; j < hunk.lines.length; j++) {
      var line = hunk.lines[j],
          operation = line[0],
          content = line.substr(1);

      if (operation === ' ' || operation === '-') {
        // Context sanity check
        if (!compareLine(toPos + 1, lines[toPos], operation, content)) {
          errorCount++;

          if (errorCount > fuzzFactor) {
            return false;
          }
        }
        toPos++;
      }
    }

    return true;
  }

  // Search best fit offsets for each hunk based on the previous ones
  for (var i = 0; i < hunks.length; i++) {
    var hunk = hunks[i],
        maxLine = lines.length - hunk.oldLines,
        localOffset = 0,
        toPos = offset + hunk.oldStart - 1;

    var iterator = /*istanbul ignore start*/(0, _distanceIterator2['default']) /*istanbul ignore end*/(toPos, minLine, maxLine);

    for (; localOffset !== undefined; localOffset = iterator()) {
      if (hunkFits(hunk, toPos + localOffset)) {
        hunk.offset = offset += localOffset;
        break;
      }
    }

    if (localOffset === undefined) {
      return false;
    }

    // Set lower text limit to end of the current hunk, so next ones don't try
    // to fit over already patched text
    minLine = hunk.offset + hunk.oldStart + hunk.oldLines;
  }

  // Apply patch hunks
  for (var _i = 0; _i < hunks.length; _i++) {
    var _hunk = hunks[_i],
        _toPos = _hunk.offset + _hunk.newStart - 1;
    if (_hunk.newLines == 0) {
      _toPos++;
    }

    for (var j = 0; j < _hunk.lines.length; j++) {
      var line = _hunk.lines[j],
          operation = line[0],
          content = line.substr(1),
          delimiter = _hunk.linedelimiters[j];

      if (operation === ' ') {
        _toPos++;
      } else if (operation === '-') {
        lines.splice(_toPos, 1);
        delimiters.splice(_toPos, 1);
        /* istanbul ignore else */
      } else if (operation === '+') {
          lines.splice(_toPos, 0, content);
          delimiters.splice(_toPos, 0, delimiter);
          _toPos++;
        } else if (operation === '\\') {
          var previousOperation = _hunk.lines[j - 1] ? _hunk.lines[j - 1][0] : null;
          if (previousOperation === '+') {
            removeEOFNL = true;
          } else if (previousOperation === '-') {
            addEOFNL = true;
          }
        }
    }
  }

  // Handle EOFNL insertion/removal
  if (removeEOFNL) {
    while (!lines[lines.length - 1]) {
      lines.pop();
      delimiters.pop();
    }
  } else if (addEOFNL) {
    lines.push('');
    delimiters.push('\n');
  }
  for (var _k = 0; _k < lines.length - 1; _k++) {
    lines[_k] = lines[_k] + delimiters[_k];
  }
  return lines.join('');
}
```
- example usage
```shell
...
  hunks: [{
    oldStart: 1, oldLines: 3, newStart: 1, newLines: 3,
    lines: [' line2', ' line3', '-line4', '+line5', '\\ No newline at end of file'],
  }]
}
'''

* 'JsDiff.applyPatch(source, patch[, options])' - applies a unified diff patch.

Return a string containing new version of provided data. 'patch' may be a string diff or the output from the 'parsePatch' or 'structuredPatch
' methods.

The optional 'options' object may have the following keys:

- 'fuzzFactor': Number of lines that are allowed to differ before rejecting a patch. Defaults to 0.
- 'compareLine(lineNumber, line, operation, patchContent)': Callback used to compare to given lines to determine if they should
be considered equal when patching. Defaults to strict equality but may be overriden to provide fuzzier comparison. Should return
 false if the lines should be rejected.
...
```

#### <a name="apidoc.element.diff.applyPatches"></a>[function <span class="apidocSignatureSpan">diff.</span>applyPatches (uniDiff, options)](#apidoc.element.diff.applyPatches)
- description and source-code
```javascript
function applyPatches(uniDiff, options) {
  if (typeof uniDiff === 'string') {
    uniDiff = /*istanbul ignore start*/(0, _parse.parsePatch) /*istanbul ignore end*/(uniDiff);
  }

  var currentIndex = 0;
  function processIndex() {
    var index = uniDiff[currentIndex++];
    if (!index) {
      return options.complete();
    }

    options.loadFile(index, function (err, data) {
      if (err) {
        return options.complete(err);
      }

      var updatedContent = applyPatch(data, index, options);
      options.patched(index, updatedContent, function (err) {
        if (err) {
          return options.complete(err);
        }

        processIndex();
      });
    });
  }
  processIndex();
}
```
- example usage
```shell
...
Return a string containing new version of provided data. 'patch' may be a string diff or the output from the 'parsePatch' or 'structuredPatch
' methods.

The optional 'options' object may have the following keys:

- 'fuzzFactor': Number of lines that are allowed to differ before rejecting a patch. Defaults to 0.
- 'compareLine(lineNumber, line, operation, patchContent)': Callback used to compare to given lines to determine if they should
be considered equal when patching. Defaults to strict equality but may be overriden to provide fuzzier comparison. Should return
 false if the lines should be rejected.

* 'JsDiff.applyPatches(patch, options)' - applies one or more patches.

This method will iterate over the contents of the patch and apply to data provided through callbacks. The general flow for each
patch index is:

- 'options.loadFile(index, callback)' is called. The caller should then load the contents of the file and then pass that to the '
callback(err, data)' callback. Passing an 'err' will terminate further patch execution.
- 'options.patched(index, content, callback)' is called once the patch has been applied. 'content' will be the return value from
 'applyPatch'. When it's ready, the caller should call 'callback(err)' callback. Passing an 'err' will terminate further patch execution
.

Once all patches have been applied or an error occurs, the 'options.complete(err)' callback is made.
...
```

#### <a name="apidoc.element.diff.canonicalize"></a>[function <span class="apidocSignatureSpan">diff.</span>canonicalize (obj, stack, replacementStack)](#apidoc.element.diff.canonicalize)
- description and source-code
```javascript
function canonicalize(obj, stack, replacementStack) {
  stack = stack || [];
  replacementStack = replacementStack || [];

  var i =<span class="apidocCodeCommentSpan"> /*istanbul ignore start*/void 0 /*istanbul ignore end*/;

  for (i = 0; i < stack.length; i += 1) {
    if (stack[i] === obj) {
      return replacementStack[i];
    }
  }

  var canonicalizedObj = /*istanbul ignore start*/void 0 /*istanbul ignore end*/;

  if ('[object Array]' === objectPrototypeToString.call(obj)) {
    stack.push(obj);
    canonicalizedObj = new Array(obj.length);
    replacementStack.push(canonicalizedObj);
    for (i = 0; i < obj.length; i += 1) {
      canonicalizedObj[i] = canonicalize(obj[i], stack, replacementStack);
    }
    stack.pop();
    replacementStack.pop();
    return canonicalizedObj;
  }

  if (obj && obj.toJSON) {
    obj = obj.toJSON();
  }

  if ( /*istanbul ignore start*/(typeof /*istanbul ignore end*/obj === 'undefined' ? 'undefined' : _typeof(obj)) === 'object' &&
obj !== null) {
    stack.push(obj);
    canonicalizedObj = {};
    replacementStack.push(canonicalizedObj);
    var sortedKeys = [],
        key = /*istanbul ignore start*/void 0 /*istanbul ignore end*/;
    for (key in obj) {
      /* istanbul ignore else */
</span>      if (obj.hasOwnProperty(key)) {
        sortedKeys.push(key);
      }
    }
    sortedKeys.sort();
    for (i = 0; i < sortedKeys.length; i += 1) {
      key = sortedKeys[i];
      canonicalizedObj[key] = canonicalize(obj[key], stack, replacementStack);
    }
    stack.pop();
    replacementStack.pop();
  } else {
    canonicalizedObj = obj;
  }
  return canonicalizedObj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.convertChangesToDMP"></a>[function <span class="apidocSignatureSpan">diff.</span>convertChangesToDMP (changes)](#apidoc.element.diff.convertChangesToDMP)
- description and source-code
```javascript
function convertChangesToDMP(changes) {
  var ret = [],
      change = /*istanbul ignore start*/void 0 /*istanbul ignore end*/,
      operation = /*istanbul ignore start*/void 0 /*istanbul ignore end*/;
  for (var i = 0; i < changes.length; i++) {
    change = changes[i];
    if (change.added) {
      operation = 1;
    } else if (change.removed) {
      operation = -1;
    } else {
      operation = 0;
    }

    ret.push([operation, change.value]);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.convertChangesToXML"></a>[function <span class="apidocSignatureSpan">diff.</span>convertChangesToXML (changes)](#apidoc.element.diff.convertChangesToXML)
- description and source-code
```javascript
function convertChangesToXML(changes) {
  var ret = [];
  for (var i = 0; i < changes.length; i++) {
    var change = changes[i];
    if (change.added) {
      ret.push('<ins>');
    } else if (change.removed) {
      ret.push('<del>');
    }

    ret.push(escapeHTML(change.value));

    if (change.added) {
      ret.push('</ins>');
    } else if (change.removed) {
      ret.push('</del>');
    }
  }
  return ret.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.createPatch"></a>[function <span class="apidocSignatureSpan">diff.</span>createPatch (fileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.createPatch)
- description and source-code
```javascript
function createPatch(fileName, oldStr, newStr, oldHeader, newHeader, options) {
  return createTwoFilesPatch(fileName, fileName, oldStr, newStr, oldHeader, newHeader, options);
}
```
- example usage
```shell
...
* 'newFileName' : String to be output in the filename section of the patch for the additions
* 'oldStr' : Original string value
* 'newStr' : New string value
* 'oldHeader' : Additional information to include in the old file header
* 'newHeader' : Additional information to include in the new file header
* 'options' : An object with options. Currently, only 'context' is supported and describes how many lines of context should be included
.

* 'JsDiff.createPatch(fileName, oldStr, newStr, oldHeader, newHeader)' - creates a unified diff patch.

Just like JsDiff.createTwoFilesPatch, but with oldFileName being equal to newFileName.


* 'JsDiff.structuredPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)' - returns an object with an
array of hunk objects.

This method is similar to createTwoFilesPatch, but returns a data structure
...
```

#### <a name="apidoc.element.diff.createTwoFilesPatch"></a>[function <span class="apidocSignatureSpan">diff.</span>createTwoFilesPatch (oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.createTwoFilesPatch)
- description and source-code
```javascript
function createTwoFilesPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options) {
  var diff = structuredPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options);

  var ret = [];
  if (oldFileName == newFileName) {
    ret.push('Index: ' + oldFileName);
  }
  ret.push('===================================================================');
  ret.push('--- ' + diff.oldFileName + (typeof diff.oldHeader === 'undefined' ? '' : '\t' + diff.oldHeader));
  ret.push('+++ ' + diff.newFileName + (typeof diff.newHeader === 'undefined' ? '' : '\t' + diff.newHeader));

  for (var i = 0; i < diff.hunks.length; i++) {
    var hunk = diff.hunks[i];
    ret.push('@@ -' + hunk.oldStart + ',' + hunk.oldLines + ' +' + hunk.newStart + ',' + hunk.newLines + ' @@');
    ret.push.apply(ret, hunk.lines);
  }

  return ret.join('\n') + '\n';
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffArrays(oldArr, newArr[, options])' - diffs two arrays, comparing each item for strict equality (===).

Returns a list of change objects (See below).

* 'JsDiff.createTwoFilesPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader)' - creates a unified diff patch.

Parameters:
* 'oldFileName' : String to be output in the filename section of the patch for the removals
* 'newFileName' : String to be output in the filename section of the patch for the additions
* 'oldStr' : Original string value
* 'newStr' : New string value
* 'oldHeader' : Additional information to include in the old file header
...
```

#### <a name="apidoc.element.diff.diffArrays"></a>[function <span class="apidocSignatureSpan">diff.</span>diffArrays (oldArr, newArr, callback)](#apidoc.element.diff.diffArrays)
- description and source-code
```javascript
function diffArrays(oldArr, newArr, callback) {
  return arrayDiff.diff(oldArr, newArr, callback);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffJson(oldObj, newObj[, options])' - diffs two JSON objects, comparing the fields defined on each. The order of fields
, etc does not matter in this comparison.

Returns a list of change objects (See below).

* 'JsDiff.diffArrays(oldArr, newArr[, options])' - diffs two arrays, comparing each item for strict equality (===).

Returns a list of change objects (See below).

* 'JsDiff.createTwoFilesPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader)' - creates a unified diff patch.

Parameters:
* 'oldFileName' : String to be output in the filename section of the patch for the removals
...
```

#### <a name="apidoc.element.diff.diffChars"></a>[function <span class="apidocSignatureSpan">diff.</span>diffChars (oldStr, newStr, callback)](#apidoc.element.diff.diffChars)
- description and source-code
```javascript
function diffChars(oldStr, newStr, callback) {
  return characterDiff.diff(oldStr, newStr, callback);
}
```
- example usage
```shell
...
or

bower install jsdiff


## API

* 'JsDiff.diffChars(oldStr, newStr[, options])' - diffs two blocks of text, comparing character by character.

Returns a list of change objects (See below).

* 'JsDiff.diffWords(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, ignoring whitespace.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffCss"></a>[function <span class="apidocSignatureSpan">diff.</span>diffCss (oldStr, newStr, callback)](#apidoc.element.diff.diffCss)
- description and source-code
```javascript
function diffCss(oldStr, newStr, callback) {
  return cssDiff.diff(oldStr, newStr, callback);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffSentences(oldStr, newStr[, options])' - diffs two blocks of text, comparing sentence by sentence.

Returns a list of change objects (See below).

* 'JsDiff.diffCss(oldStr, newStr[, options])' - diffs two blocks of text, comparing CSS tokens.

Returns a list of change objects (See below).

* 'JsDiff.diffJson(oldObj, newObj[, options])' - diffs two JSON objects, comparing the fields defined on each. The order of fields
, etc does not matter in this comparison.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffJson"></a>[function <span class="apidocSignatureSpan">diff.</span>diffJson (oldObj, newObj, options)](#apidoc.element.diff.diffJson)
- description and source-code
```javascript
function diffJson(oldObj, newObj, options) {
  return jsonDiff.diff(oldObj, newObj, options);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffCss(oldStr, newStr[, options])' - diffs two blocks of text, comparing CSS tokens.

Returns a list of change objects (See below).

* 'JsDiff.diffJson(oldObj, newObj[, options])' - diffs two JSON objects, comparing the fields defined on each. The order of fields
, etc does not matter in this comparison.

Returns a list of change objects (See below).

* 'JsDiff.diffArrays(oldArr, newArr[, options])' - diffs two arrays, comparing each item for strict equality (===).

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffLines"></a>[function <span class="apidocSignatureSpan">diff.</span>diffLines (oldStr, newStr, callback)](#apidoc.element.diff.diffLines)
- description and source-code
```javascript
function diffLines(oldStr, newStr, callback) {
  return lineDiff.diff(oldStr, newStr, callback);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffWordsWithSpace(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, treating whitespace
 as significant.

Returns a list of change objects (See below).

* 'JsDiff.diffLines(oldStr, newStr[, options])' - diffs two blocks of text, comparing line by line.

Options
* 'ignoreWhitespace': 'true' to ignore leading and trailing whitespace. This is the same as 'diffTrimmedLines'
* 'newlineIsToken': 'true' to treat newline characters as separate tokens.  This allows for changes to the newline structure to
occur independently of the line content and to be treated as such. In general this is the more human friendly form of 'diffLines
' and 'diffLines' is better suited for patches and other computer friendly output.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffSentences"></a>[function <span class="apidocSignatureSpan">diff.</span>diffSentences (oldStr, newStr, callback)](#apidoc.element.diff.diffSentences)
- description and source-code
```javascript
function diffSentences(oldStr, newStr, callback) {
  return sentenceDiff.diff(oldStr, newStr, callback);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffTrimmedLines(oldStr, newStr[, options])' - diffs two blocks of text, comparing line by line, ignoring leading and
trailing whitespace.

Returns a list of change objects (See below).

* 'JsDiff.diffSentences(oldStr, newStr[, options])' - diffs two blocks of text, comparing sentence by sentence.

Returns a list of change objects (See below).

* 'JsDiff.diffCss(oldStr, newStr[, options])' - diffs two blocks of text, comparing CSS tokens.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffTrimmedLines"></a>[function <span class="apidocSignatureSpan">diff.</span>diffTrimmedLines (oldStr, newStr, callback)](#apidoc.element.diff.diffTrimmedLines)
- description and source-code
```javascript
function diffTrimmedLines(oldStr, newStr, callback) {
  var options = /*istanbul ignore start*/(0, _params.generateOptions) /*istanbul ignore end*/(callback, { ignoreWhitespace: true
 });
  return lineDiff.diff(oldStr, newStr, options);
}
```
- example usage
```shell
...

Options
* 'ignoreWhitespace': 'true' to ignore leading and trailing whitespace. This is the same as 'diffTrimmedLines'
* 'newlineIsToken': 'true' to treat newline characters as separate tokens.  This allows for changes to the newline structure to
occur independently of the line content and to be treated as such. In general this is the more human friendly form of 'diffLines
' and 'diffLines' is better suited for patches and other computer friendly output.

Returns a list of change objects (See below).

* 'JsDiff.diffTrimmedLines(oldStr, newStr[, options])' - diffs two blocks of text, comparing line by line, ignoring leading and
trailing whitespace.

Returns a list of change objects (See below).

* 'JsDiff.diffSentences(oldStr, newStr[, options])' - diffs two blocks of text, comparing sentence by sentence.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffWords"></a>[function <span class="apidocSignatureSpan">diff.</span>diffWords (oldStr, newStr, callback)](#apidoc.element.diff.diffWords)
- description and source-code
```javascript
function diffWords(oldStr, newStr, callback) {
  var options = /*istanbul ignore start*/(0, _params.generateOptions) /*istanbul ignore end*/(callback, { ignoreWhitespace: true
 });
  return wordDiff.diff(oldStr, newStr, options);
}
```
- example usage
```shell
...

## API

* 'JsDiff.diffChars(oldStr, newStr[, options])' - diffs two blocks of text, comparing character by character.

Returns a list of change objects (See below).

* 'JsDiff.diffWords(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, ignoring whitespace.

Returns a list of change objects (See below).

* 'JsDiff.diffWordsWithSpace(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, treating whitespace
 as significant.

Returns a list of change objects (See below).
...
```

#### <a name="apidoc.element.diff.diffWordsWithSpace"></a>[function <span class="apidocSignatureSpan">diff.</span>diffWordsWithSpace (oldStr, newStr, callback)](#apidoc.element.diff.diffWordsWithSpace)
- description and source-code
```javascript
function diffWordsWithSpace(oldStr, newStr, callback) {
  return wordDiff.diff(oldStr, newStr, callback);
}
```
- example usage
```shell
...

Returns a list of change objects (See below).

* 'JsDiff.diffWords(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, ignoring whitespace.

Returns a list of change objects (See below).

* 'JsDiff.diffWordsWithSpace(oldStr, newStr[, options])' - diffs two blocks of text, comparing word by word, treating whitespace
 as significant.

Returns a list of change objects (See below).

* 'JsDiff.diffLines(oldStr, newStr[, options])' - diffs two blocks of text, comparing line by line.

Options
* 'ignoreWhitespace': 'true' to ignore leading and trailing whitespace. This is the same as 'diffTrimmedLines'
...
```

#### <a name="apidoc.element.diff.parsePatch"></a>[function <span class="apidocSignatureSpan">diff.</span>parsePatch (uniDiff)](#apidoc.element.diff.parsePatch)
- description and source-code
```javascript
function parsePatch(uniDiff) {
  /*istanbul ignore start*/var /*istanbul ignore end*/options = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments
[1];

  var diffstr = uniDiff.split(/\r\n|[\n\v\f\r\x85]/),
      delimiters = uniDiff.match(/\r\n|[\n\v\f\r\x85]/g) || [],
      list = [],
      i = 0;

  function parseIndex() {
    var index = {};
    list.push(index);

    // Parse diff metadata
    while (i < diffstr.length) {
      var line = diffstr[i];

      // File header found, end parsing diff metadata
      if (/^(\-\-\-|\+\+\+|@@)\s/.test(line)) {
        break;
      }

      // Diff index
      var header = /^(?:Index:|diff(?: -r \w+)+)\s+(.+?)\s*$/.exec(line);
      if (header) {
        index.index = header[1];
      }

      i++;
    }

    // Parse file headers if they are defined. Unified diff requires them, but
    // there's no technical issues to have an isolated hunk without file header
    parseFileHeader(index);
    parseFileHeader(index);

    // Parse hunks
    index.hunks = [];

    while (i < diffstr.length) {
      var _line = diffstr[i];

      if (/^(Index:|diff|\-\-\-|\+\+\+)\s/.test(_line)) {
        break;
      } else if (/^@@/.test(_line)) {
        index.hunks.push(parseHunk());
      } else if (_line && options.strict) {
        // Ignore unexpected content unless in strict mode
        throw new Error('Unknown line ' + (i + 1) + ' ' + JSON.stringify(_line));
      } else {
        i++;
      }
    }
  }

  // Parses the --- and +++ headers, if none are found, no lines
  // are consumed.
  function parseFileHeader(index) {
    var headerPattern = /^(---|\+\+\+)\s+([\S ]*)(?:\t(.*?)\s*)?$/;
    var fileHeader = headerPattern.exec(diffstr[i]);
    if (fileHeader) {
      var keyPrefix = fileHeader[1] === '---' ? 'old' : 'new';
      index[keyPrefix + 'FileName'] = fileHeader[2];
      index[keyPrefix + 'Header'] = fileHeader[3];

      i++;
    }
  }

  // Parses a hunk
  // This assumes that we are at the start of a hunk.
  function parseHunk() {
    var chunkHeaderIndex = i,
        chunkHeaderLine = diffstr[i++],
        chunkHeader = chunkHeaderLine.split(/@@ -(\d+)(?:,(\d+))? \+(\d+)(?:,(\d+))? @@/);

    var hunk = {
      oldStart: +chunkHeader[1],
      oldLines: +chunkHeader[2] || 1,
      newStart: +chunkHeader[3],
      newLines: +chunkHeader[4] || 1,
      lines: [],
      linedelimiters: []
    };

    var addCount = 0,
        removeCount = 0;
    for (; i < diffstr.length; i++) {
      // Lines starting with '---' could be mistaken for the "remove line" operation
      // But they could be the header for the next file. Therefore prune such cases out.
      if (diffstr[i].indexOf('--- ') === 0 && i + 2 < diffstr.length && diffstr[i + 1].indexOf('+++ ') === 0 && diffstr[i + 2].indexOf
('@@') === 0) {
        break;
      }
      var operation = diffstr[i][0];

      if (operation === '+' || operation === '-' || operation === ' ' || operation === '\\') {
        hunk.lines.push(diffstr[i]);
        hunk.linedelimiters.push(delimiters[i] || '\n');

        if (operation === '+') {
          addCount++;
        } else if (operation === '-') {
          removeCount++;
        } else if (operation === ' ') {
          addCount++;
          removeCount++;
        }
      } else {
        break;
      }
    }

    // Handle the empty block count case
    if (!addCount && hunk.newLines === 1) {
      hunk.newLines = 0;
    }
    if (!removeCount && hunk.oldLines === 1) {
      hunk.oldLines = 0;
    }

    // Perform optional sanity checking
    if (options.strict) {
      if (addCount !== hunk.newLines) {
        throw new Error('Added line count did not match for hunk at line ' + (chunkHeaderIndex + 1));
      }
      if (removeCount !== hunk.oldLines) {
        throw new Error('Removed line count did not match for hunk at line ' + (chunkHeaderIndex + 1));
      }
    }

    return hunk;
  }

  while (i < diffstr.length) {
    parseIndex();
  }

  return list;
}
```
- example usage
```shell
...
    This method will iterate over the contents of the patch and apply to data provided through callbacks. The general flow for each
 patch index is:

    - 'options.loadFile(index, callback)' is called. The caller should then load the contents of the file and then pass that to
the 'callback(err, data)' callback. Passing an 'err' will terminate further patch execution.
    - 'options.patched(index, content, callback)' is called once the patch has been applied. 'content' will be the return value
from 'applyPatch'. When it's ready, the caller should call 'callback(err)' callback. Passing an 'err' will terminate further patch
 execution.

    Once all patches have been applied or an error occurs, the 'options.complete(err)' callback is made.

* 'JsDiff.parsePatch(diffStr)' - Parses a patch into structured data

    Return a JSON object representation of the a patch, suitable for use with the 'applyPatch' method. This parses to the same structure
 returned by 'JsDiff.structuredPatch'.

* 'convertChangesToXML(changes)' - converts a list of changes to a serialized XML format


All methods above which accept the optional 'callback' method will run in sync mode when that parameter is omitted and in async
mode when supplied. This allows for larger diffs without blocking the event loop. This may be passed either directly as the final
 parameter or as the 'callback' field in the 'options' object.
...
```

#### <a name="apidoc.element.diff.structuredPatch"></a>[function <span class="apidocSignatureSpan">diff.</span>structuredPatch (oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)](#apidoc.element.diff.structuredPatch)
- description and source-code
```javascript
function structuredPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options) {
  if (!options) {
    options = {};
  }
  if (typeof options.context === 'undefined') {
    options.context = 4;
  }

  var diff =<span class="apidocCodeCommentSpan"> /*istanbul ignore start*/(0, _line.diffLines) /*istanbul ignore end*/(oldStr, newStr, options);
  diff.push({ value: '', lines: [] }); // Append an empty value to make cleanup easier

  function contextLines(lines) {
    return lines.map(function (entry) {
      return ' ' + entry;
    });
  }

  var hunks = [];
  var oldRangeStart = 0,
      newRangeStart = 0,
      curRange = [],
      oldLine = 1,
      newLine = 1;
  /*istanbul ignore start*/
</span>  var _loop = function _loop( /*istanbul ignore end*/i) {
    var current = diff[i],
        lines = current.lines || current.value.replace(/\n$/, '').split('\n');
    current.lines = lines;

    if (current.added || current.removed) {
      /*istanbul ignore start*/
      var _curRange;

      /*istanbul ignore end*/
      // If we have previous context, start with that
      if (!oldRangeStart) {
        var prev = diff[i - 1];
        oldRangeStart = oldLine;
        newRangeStart = newLine;

        if (prev) {
          curRange = options.context > 0 ? contextLines(prev.lines.slice(-options.context)) : [];
          oldRangeStart -= curRange.length;
          newRangeStart -= curRange.length;
        }
      }

      // Output our changes
      /*istanbul ignore start*/(_curRange = /*istanbul ignore end*/curRange).push. /*istanbul ignore start*/apply /*istanbul ignore
 end*/( /*istanbul ignore start*/_curRange /*istanbul ignore end*/, /*istanbul ignore start*/_toConsumableArray( /*istanbul ignore
 end*/lines.map(function (entry) {
        return (current.added ? '+' : '-') + entry;
      })));

      // Track the updated file position
      if (current.added) {
        newLine += lines.length;
      } else {
        oldLine += lines.length;
      }
    } else {
      // Identical context lines. Track line changes
      if (oldRangeStart) {
        // Close out any changes that have been output (or join overlapping)
        if (lines.length <= options.context * 2 && i < diff.length - 2) {
          /*istanbul ignore start*/
          var _curRange2;

          /*istanbul ignore end*/
          // Overlapping
          /*istanbul ignore start*/(_curRange2 = /*istanbul ignore end*/curRange).push. /*istanbul ignore start*/apply /*istanbul
 ignore end*/( /*istanbul ignore start*/_curRange2 /*istanbul ignore end*/, /*istanbul ignore start*/_toConsumableArray( /*istanbul
 ignore end*/contextLines(lines)));
        } else {
          /*istanbul ignore start*/
          var _curRange3;

          /*istanbul ignore end*/
          // end the range and output
          var contextSize = Math.min(lines.length, options.context);
          /*istanbul ignore start*/(_curRange3 = /*istanbul ignore end*/curRange).push. /*istanbul ignore start*/apply /*istanbul
 ignore end*/( /*istanbul ignore start*/_curRange3 /*istanbul ignore end*/, /*istanbul ignore start*/_toConsumableArray( /*istanbul
 ignore end*/contextLines(lines.slice(0, contextSize))));

          var hunk = {
            oldStart: oldRangeStart,
            oldLines: oldLine - oldRangeStart + contextSize,
            newStart: newRangeStart,
            newLines: newLine - newRangeStart + contextSize,
            lines: curRange
          };
          if (i >= diff.length - 2 && lines.length <= options.context) {
            // EOF is inside this hunk
            var oldEOFNewline = /\n$/.test(oldStr);
            var newEOFNewline = /\n$/.test(newStr);
            if (lines.length == 0 && !oldEOFNewline) {
              // special case: old has no eol and no trailing context; no-nl can end up before adds
              curRange.splice(hunk.oldLines, 0, '\\ No newline at end of file');
            } else if (!oldEOFNewline || !newEOFNewline) {
              curRange.push('\\ No newline at end of file');
            }
          }
          hunks.push(hunk);

          oldRangeStart = 0;
          newRange ...
```
- example usage
```shell
...
* 'options' : An object with options. Currently, only 'context' is supported and describes how many lines of context should be included
.

* 'JsDiff.createPatch(fileName, oldStr, newStr, oldHeader, newHeader)' - creates a unified diff patch.

Just like JsDiff.createTwoFilesPatch, but with oldFileName being equal to newFileName.


* 'JsDiff.structuredPatch(oldFileName, newFileName, oldStr, newStr, oldHeader, newHeader, options)' - returns an object with an
array of hunk objects.

This method is similar to createTwoFilesPatch, but returns a data structure
suitable for further processing. Parameters are the same as createTwoFilesPatch. The data structure returned may look like this:

'''js
{
  oldFileName: 'oldfile', newFileName: 'newfile',
...
```



# <a name="apidoc.module.diff.Diff"></a>[module diff.Diff](#apidoc.module.diff.Diff)

#### <a name="apidoc.element.diff.Diff.Diff"></a>[function <span class="apidocSignatureSpan">diff.</span>Diff ()](#apidoc.element.diff.Diff.Diff)
- description and source-code
```javascript
function Diff() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.diff.Diff.prototype"></a>[module diff.Diff.prototype](#apidoc.module.diff.Diff.prototype)

#### <a name="apidoc.element.diff.Diff.prototype.castInput"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>castInput (value)](#apidoc.element.diff.Diff.prototype.castInput)
- description and source-code
```javascript
function castInput(value) {
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.diff"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>diff (oldString, newString)](#apidoc.element.diff.Diff.prototype.diff)
- description and source-code
```javascript
function diff(oldString, newString) {
<span class="apidocCodeCommentSpan">  /*istanbul ignore start*/var /*istanbul ignore end*/options = arguments.length <= 2 || arguments[2] === undefined ? {} : arguments
[2];

  var callback = options.callback;
  if (typeof options === 'function') {
    callback = options;
    options = {};
  }
  this.options = options;

  var self = this;

  function done(value) {
    if (callback) {
      setTimeout(function () {
        callback(undefined, value);
      }, 0);
      return true;
    } else {
      return value;
    }
  }

  // Allow subclasses to massage the input prior to running
  oldString = this.castInput(oldString);
  newString = this.castInput(newString);

  oldString = this.removeEmpty(this.tokenize(oldString));
  newString = this.removeEmpty(this.tokenize(newString));

  var newLen = newString.length,
      oldLen = oldString.length;
  var editLength = 1;
  var maxEditLength = newLen + oldLen;
  var bestPath = [{ newPos: -1, components: [] }];

  // Seed editLength = 0, i.e. the content starts with the same values
  var oldPos = this.extractCommon(bestPath[0], newString, oldString, 0);
  if (bestPath[0].newPos + 1 >= newLen && oldPos + 1 >= oldLen) {
    // Identity per the equality and tokenizer
    return done([{ value: this.join(newString), count: newString.length }]);
  }

  // Main worker method. checks all permutations of a given edit length for acceptance.
  function execEditLength() {
    for (var diagonalPath = -1 * editLength; diagonalPath <= editLength; diagonalPath += 2) {
      var basePath = /*istanbul ignore start*/void 0 /*istanbul ignore end*/;
      var addPath = bestPath[diagonalPath - 1],
          removePath = bestPath[diagonalPath + 1],
          _oldPos = (removePath ? removePath.newPos : 0) - diagonalPath;
      if (addPath) {
        // No one else is going to attempt to use this value, clear it
        bestPath[diagonalPath - 1] = undefined;
      }

      var canAdd = addPath && addPath.newPos + 1 < newLen,
          canRemove = removePath && 0 <= _oldPos && _oldPos < oldLen;
      if (!canAdd && !canRemove) {
        // If this path is a terminal then prune
        bestPath[diagonalPath] = undefined;
        continue;
      }

      // Select the diagonal that we want to branch from. We select the prior
      // path whose position in the new string is the farthest from the origin
      // and does not pass the bounds of the diff graph
      if (!canAdd || canRemove && addPath.newPos < removePath.newPos) {
        basePath = clonePath(removePath);
        self.pushComponent(basePath.components, undefined, true);
      } else {
        basePath = addPath; // No need to clone, we've pulled it from the list
        basePath.newPos++;
        self.pushComponent(basePath.components, true, undefined);
      }

      _oldPos = self.extractCommon(basePath, newString, oldString, diagonalPath);

      // If we have hit the end of both strings, then we are done
      if (basePath.newPos + 1 >= newLen && _oldPos + 1 >= oldLen) {
        return done(buildValues(self, basePath.components, newString, oldString, self.useLongestToken));
      } else {
        // Otherwise track this path as a potential candidate and continue.
        bestPath[diagonalPath] = basePath;
      }
    }

    editLength++;
  }

  // Performs the length of edit iteration. Is a bit fugly as this has to support the
  // sync and async mode which is never fun. Loops over execEditLength until a value
  // is produced.
  if (callback) {
    (function exec() {
      setTimeout(function () {
        // This should not happen, but we want to be safe.
        /* istanbul ignore next */
</span>        if (editLength > maxEditLength) {
          return callback();
        }

        if (!execEditLength()) {
          exec();
        }
      }, 0);
    })();
  } else {
    while (editLength <= maxEditLength) {
      var ret = execEditLength();
      if (ret) {
        return ret;
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.equals"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>equals (left, right)](#apidoc.element.diff.Diff.prototype.equals)
- description and source-code
```javascript
function equals(left, right) {
  return left === right;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.extractCommon"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>extractCommon (basePath, newString, oldString, diagonalPath)](#apidoc.element.diff.Diff.prototype.extractCommon)
- description and source-code
```javascript
function extractCommon(basePath, newString, oldString, diagonalPath) {
  var newLen = newString.length,
      oldLen = oldString.length,
      newPos = basePath.newPos,
      oldPos = newPos - diagonalPath,
      commonCount = 0;
  while (newPos + 1 < newLen && oldPos + 1 < oldLen && this.equals(newString[newPos + 1], oldString[oldPos + 1])) {
    newPos++;
    oldPos++;
    commonCount++;
  }

  if (commonCount) {
    basePath.components.push({ count: commonCount });
  }

  basePath.newPos = newPos;
  return oldPos;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.join"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>join (chars)](#apidoc.element.diff.Diff.prototype.join)
- description and source-code
```javascript
function join(chars) {
  return chars.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.pushComponent"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>pushComponent (components, added, removed)](#apidoc.element.diff.Diff.prototype.pushComponent)
- description and source-code
```javascript
function pushComponent(components, added, removed) {
  var last = components[components.length - 1];
  if (last && last.added === added && last.removed === removed) {
    // We need to clone here as the component clone operation is just
    // as shallow array clone
    components[components.length - 1] = { count: last.count + 1, added: added, removed: removed };
  } else {
    components.push({ count: 1, added: added, removed: removed });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.removeEmpty"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>removeEmpty (array)](#apidoc.element.diff.Diff.prototype.removeEmpty)
- description and source-code
```javascript
function removeEmpty(array) {
  var ret = [];
  for (var i = 0; i < array.length; i++) {
    if (array[i]) {
      ret.push(array[i]);
    }
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.diff.Diff.prototype.tokenize"></a>[function <span class="apidocSignatureSpan">diff.Diff.prototype.</span>tokenize (value)](#apidoc.element.diff.Diff.prototype.tokenize)
- description and source-code
```javascript
function tokenize(value) {
  return value.split('');
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
