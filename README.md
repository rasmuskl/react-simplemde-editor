# React SimpleMDE Markdown Editor
[![NPM version][npm-badge]][npm]

React component wrapper for
[SimpleMDE](https://github.com/NextStepWebs/simplemde-markdown-editor).

## Contribute
This is a WIP, if you find this component useful, contributions are appreciated, [see issues](https://github.com/benrlodge/react-simplemde-editor/issues). 

## New in version 3.0
The `initialValue` prop has been removed and replaced with a `value` prop, allowing direct changes to the value to be made after the component mounts.

## New in version 2.0
Version 1.0 did not have SimpleMDE options configured well, this readme reflects the changes made to better include options.
This is still a very new project. Testing, feedback and PRs are welcome and appreciated.

## Install
```
npm install --save react-simplemde-editor
```

## Demo
http://www.benrlodge.com/projects/react-simplemde

or view it locally:
```
git clone https://github.com/benrlodge/react-simplemde-editor.git
cd react-simplemde-editor
npm install
cd demo
gulp
open browser to localhost:3000
```

## Usage
View the [demo code](https://github.com/benrlodge/react-simplemde-editor/tree/master/demo/scripts) for a full example.

Not required, but useless without it, the `onChange` callback is the only option you need to set.

```javascript
var React = require('react');
var SimpleMDE = require('react-simplemde-editor');

<SimpleMDE
  onChange={this.handleChange}
/>
```

## Options
Set additional [SimpleMDE options](https://github.com/NextStepWebs/simplemde-markdown-editor#configuration) with an options prop.

Note - while SimpleMDE options has an `initialValue` option, this component only takes a `value` prop which is set as the `initialValue` on first render.

```javascript
var React = require('react');
var SimpleMDE = require('react-simplemde-editor');

<SimpleMDEReact
  onChange={this.handleChange}
  options={{
    autofocus: true,
    spellChecker: false,
    value: this.state.textValue
    // etc.
  }}
/>
```

[npm-badge]: http://badge.fury.io/js/react-simplemde-editor.svg
[npm]: http://badge.fury.io/js/react-simplemde-editor
