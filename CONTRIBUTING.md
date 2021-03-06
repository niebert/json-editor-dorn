
## Contributing
This document briefly lists the guidelines for contributing to JSON Editor.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Contributing](#contributing)
  - [Reporting Bugs](#reporting-bugs)
  - [Contributing Code](#contributing-code)
    - [Code Style](#code-style)
    - [Submitting Pull Requests](#submitting-pull-requests)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Reporting Bugs

When creating an issue in GitHub, try to include when feasible:
*  A brief description of the issue
*  An example JSON schema that causes the issue
*  Steps to reproduce

If you can reproduce the issue on the demo page (http://jeremydorn.com/json-editor/), it's helpful to attach the "Direct Link" url (top right of page).  Note: the direct link might not work for very large schemas or JSON values.


## Contributing Code
One of the major goals of JSON Editor is to be easy to modify and hack.

If you fix a bug or add a cool feature, please submit a pull request!


## Code Style

*  Use 2 spaces for indentation
*  Use comments whenever the code's meaning is not obvious
*  When in doubt, try to match the style in existing source files

## Browserify/Watchify

The easiest way to hack on JSON Editor is to run `npm run watch`, which
re-builds `dist/jsoneditor.js` every time a source file changes.

* To run just a new build call `npm run build`.
* If you want to automize this process after code alteration
* To test the quality of your Javascript code, call `npm run test` to run `jshint` on library.
* To minify/compress the source code run `npm run compress` which also runs a build by `node build.js`.

To do a full build which includes `jshint` run `npm run test`.

## Submitting Pull Requests
Try to limit pull requests to a single narrow feature or bug fix.

__Do not submit `dist/` files!__

The following is done when a pull request is accepted.  There is no need to do any of these steps yourself.

1.  Merge pull request into master
2.  Increment version number in `src/intro.js` and `bower.json`.  Set date in `src/intro.js`.
3.  Build `dist/` files with grunt
4.  Commit and push to github
5.  Add a git tag and release for this version with a short changelog

Sometimes, multiple pull requests will be merged before doing steps 2-5.
