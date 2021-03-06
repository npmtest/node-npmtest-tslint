# npmtest-tslint

#### basic test coverage for  [tslint (v5.1.0)](https://github.com/palantir/tslint#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-tslint.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tslint) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tslint.svg)](https://travis-ci.org/npmtest/node-npmtest-tslint)

#### An extensible static analysis linter for the TypeScript language

[![NPM](https://nodei.co/npm/tslint.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tslint)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tslint/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tslint/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tslint/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tslint/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tslint/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tslint/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tslint/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tslint/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tslint/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tslint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tslint/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tslint/build/test-report.html](https://npmtest.github.io/node-npmtest-tslint/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tslint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tslint/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tslint/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tslint/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tslint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tslint/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tslint/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tslint/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "tslint": "./bin/tslint"
    },
    "bugs": {
        "url": "https://github.com/palantir/tslint/issues"
    },
    "dependencies": {
        "babel-code-frame": "^6.22.0",
        "colors": "^1.1.2",
        "diff": "^3.2.0",
        "findup-sync": "~0.3.0",
        "glob": "^7.1.1",
        "optimist": "~0.6.0",
        "resolve": "^1.3.2",
        "semver": "^5.3.0",
        "tsutils": "^1.4.0"
    },
    "description": "An extensible static analysis linter for the TypeScript language",
    "devDependencies": {
        "@types/babel-code-frame": "^6.20.0",
        "@types/chai": "^3.4.34",
        "@types/colors": "^0.6.33",
        "@types/diff": "0.0.31",
        "@types/findup-sync": "^0.3.29",
        "@types/github": "^0.0.0",
        "@types/glob": "^5.0.30",
        "@types/js-yaml": "^3.5.29",
        "@types/mocha": "^2.2.35",
        "@types/node": "^6.0.56",
        "@types/optimist": "0.0.29",
        "@types/resolve": "0.0.4",
        "@types/semver": "^5.3.30",
        "chai": "^3.5.0",
        "github": "^8.1.1",
        "js-yaml": "^3.7.0",
        "mocha": "^3.2.0",
        "npm-run-all": "^3.1.0",
        "nyc": "^10.2.0",
        "rimraf": "^2.5.4",
        "tslint": "latest",
        "tslint-test-config-non-relative": "file:test/external/tslint-test-config-non-relative",
        "typescript": "^2.2.2"
    },
    "directories": {},
    "dist": {
        "shasum": "51a47baeeb58956fcd617bd2cf00e2ef0eea2ed9",
        "tarball": "https://registry.npmjs.org/tslint/-/tslint-5.1.0.tgz"
    },
    "engines": {
        "node": ">=4.1.2"
    },
    "homepage": "https://github.com/palantir/tslint#readme",
    "keywords": [
        "cli",
        "typescript",
        "linter"
    ],
    "license": "Apache-2.0",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "palantir"
        }
    ],
    "name": "tslint",
    "optionalDependencies": {},
    "peerDependencies": {
        "typescript": ">=2.1.0 || >=2.1.0-dev || >=2.2.0-dev || >=2.3.0-dev || >=2.4.0-dev"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/palantir/tslint.git"
    },
    "scripts": {
        "clean": "npm-run-all -p clean:core clean:test",
        "clean:core": "rimraf lib",
        "clean:test": "rimraf build && rimraf test/config/node_modules",
        "compile": "npm-run-all -p compile:core compile:test -s compile:scripts",
        "compile:core": "tsc -p src",
        "compile:scripts": "tsc -p scripts",
        "compile:test": "tsc -p test",
        "coverage": "rimraf coverage .nyc_output && nyc npm test",
        "docs": "node scripts/buildDocs.js",
        "lint": "npm-run-all -p lint:global lint:from-bin",
        "lint:from-bin": "node bin/tslint --project test/tsconfig.json --format stylish",
        "lint:global": "tslint --project test/tsconfig.json --format stylish # test includes 'src' too",
        "test": "npm-run-all test:pre -p test:mocha test:rules",
        "test:mocha": "mocha --reporter spec --colors \"build/test/**/*Tests.js\"",
        "test:pre": "cd ./test/config && npm install",
        "test:rules": "node ./build/test/ruleTestRunner.js",
        "verify": "npm-run-all clean compile lint test docs"
    },
    "typings": "./lib/index.d.ts",
    "version": "5.1.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
