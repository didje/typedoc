# TypeDoc

> Documentation generator for TypeScript projects.

[![Build Status](https://travis-ci.org/sebastian-lenz/typedoc.svg?branch=master)](https://travis-ci.org/sebastian-lenz/typedoc) [![NPM version](https://badge.fury.io/js/typedoc.svg)](http://badge.fury.io/js/typedoc)


## Installation

For unknown reasons TypeDoc do not install on some windows configuration using git or https protocol. You can install TypeDoc
in your project's directory using the latest tarball:

```bash
$ npm install https://github.com/didje/typedoc/archive/master.tar.gz --save-dev
```

Like the TypeScript compiler, TypeDoc comes with a binary that can be called from anywhere
if you install TypeDoc as a global module. The name of the executable is ``typedoc``.

```bash
$ npm install https://github.com/didje/typedoc/archive/master.tar.gz --global
$ typedoc
```


## Preview

If you want to know what a documentation created with TypeDoc looks like, head over
to the homepage of the project. We've setup examples demonstrating the two default
themes shipped with the package:

[http://typedoc.io/themes/default](http://typedoc.io/themes/default)<br>
[http://typedoc.io/themes/minimal](http://typedoc.io/themes/minimal)


## Usage

### Shell

TypeDoc accepts most of the command line arguments that the TypeScript compiler accepts. One major
difference is the fact that one may pass an entire directory instead of individual files to the documentation
generator. So in order to create a documentation for an entire project you simply type:

```bash
$ typedoc --out path/to/documentation/ path/to/typescript/project/
```

### Important note

Starting with version 0.2, TypeDoc no longer can predict whether files should be treated as modules
or whether the project should be compiled into one big namespace. You must specify the `mode` argument
in order to change the behaviour of TypeDoc.


### Arguments

* `--out <path/to/documentation/>`<br>
  Specifies the location the documentation should be written to.
* `--mode <file|modules>`<br>
  Specifies the output mode the project is used to be compiled with.
* `--json <path/to/output.json>`<br>
  Specifies the location and file name a json file describing the project is written to. When specified no documentation will be generated.

#### Source file handling
* `--exclude <pattern>`<br>
  Exclude files by the given pattern when a path is provided as source
* `--includeDeclarations`<br>
  Turn on parsing of .d.ts declaration files.
* `--externalPattern <pattern>`<br>
  Define a pattern for files that should be considered being external.
* `--excludeExternals`<br>
  Prevent externally resolved TypeScript files from being documented.

#### TypeScript compiler
* `--module <commonjs or amd>`<br>
  Specify module code generation: "commonjs" or "amd"
* `--target <ES3 or ES5>`<br>
  Specify ECMAScript target version: "ES3" (default), or "ES5"

#### Theming
* `--theme <default|minimal|path/to/theme>`<br>
  Specify the path to the theme that should be used.
* `--name <Documentation title>`<br>
  Set the name of the project that will be used in the header of the template.
* `--readme <path/to/readme|none>`<br>
  Path to the readme file that should be displayed on the index page. Pass `none` to disable the index page
  and start the documentation on the globals page.
* `--hideGenerator`<br>
  Do not print the TypeDoc link at the end of the page.
* `--gaID`<br>
  Set the Google Analytics tracking ID and activate tracking code.
* `--gaSite <site>`<br>
  Set the site name for Google Analytics. Defaults to `auto`
* `--entryPoint <fully.qualified.name>`<br>
  Specifies the fully qualified name of the root symbol. Defaults to global namespace.

#### Content
* `--includes <path/to/includes>`<br>
  Specifies the location to look for included documents. One may use <code>[[include:FILENAME]]</code>
  in comments to include documents from this location.

* `--media <path/to/media>`<br>
  Specifies the location with media files that should be copied to the output directory. In order to create
  a link to media files use the pattern <code>media://FILENAME</code> in comments.

#### Miscellaneous
* `--version`<br>
  Display the version number of TypeDoc.
* `--help`<br>
  Display a simple cheat sheet.


### Gulp

There is a plugin available to run TypeDoc with Gulp created by Rogier Schouten. You can find it on NPM:<br>
[https://www.npmjs.org/package/gulp-typedoc/](https://www.npmjs.org/package/gulp-typedoc/)


### Grunt

There is a plugin available to run TypeDoc with Grunt created by Bart van der Schoor. You can find it on NPM:<br>
[https://www.npmjs.org/package/grunt-typedoc](https://www.npmjs.org/package/grunt-typedoc)


## Advanced guides and docs

Visit our homepage for advanced guides and an extensive API documentation:<br>
[http://typedoc.io](http://typedoc.io)


## Contributing

Contributions are welcome and appreciated. You can find TypeDoc on GitHub, feel free to start
an issue or create a pull requests:<br>
[https://github.com/sebastian-lenz/typedoc](https://github.com/sebastian-lenz/typedoc)


## License

Copyright (c) 2015 [Sebastian Lenz](http://www.sebastian-lenz.de).<br>
Licensed under the Apache License 2.0.
