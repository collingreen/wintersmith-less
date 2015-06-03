
# wintersmith-less

[less](http://lesscss.org) plugin for [wintersmith](https://github.com/jnordberg/wintersmith)

install:

`npm install wintersmith-less -g`
then add `wintersmith-less` to your plugins in the wintersmith config


config:

By default, the wintersmith-less plugin matches any .less file that doesn't
start with a leading _ (the exact regex is ``). You can modify this by
setting the `fileGlob` key in the `less` section of your config.json.

For example, the settings below will change the less plugin to not automatically
include any files inside directories with a leading _. This can be useful for
including just a base file.less that imports from _folder/*.less, resulting in
just one generated .css file without having to move your source .less files
somewhere else.

~~~
  "less": {
    "fileGlob": "[^\\_]**/[^\\_]*.less"
  }
~~~
