HTMLHint-ng2
=======================

HTMLHint is a Static Code Analysis Tool for Angular 2 HTML templates, you can use it with IDE or in build system.

It extends [https://github.com/yaniswang/HTMLHint](HTMLHint) and adds support for Angular 2 attributes ie, [inputs],
(outputs), *ngDirectives, and includes rules supporting camelCase attribute names and preventing inline attributes
for better diff-ing.

[![NPM version](https://img.shields.io/npm/v/htmlhint-ng2.svg?style=flat)](https://www.npmjs.com/package/htmlhint-ng2)
[![License](https://img.shields.io/npm/l/htmlhint-ng2.svg?style=flat)](https://www.npmjs.com/package/htmlhint-ng2)
[![NPM count](https://img.shields.io/npm/dm/htmlhint-ng2.svg?style=flat)](https://www.npmjs.com/package/htmlhint-ng2)
[![NPM count](https://img.shields.io/npm/dt/htmlhint-ng2.svg?style=flat)](https://www.npmjs.com/package/htmlhint-ng2)

Quick start
======================

1. install & hint

        npm install htmlhint-ng2 -g
        htmlhint-ng2 -V
        htmlhint-ng2 --help
        htmlhint-ng2 www
        htmlhint-ng2 www/test.html
        htmlhint-ng2 www/**/*.xhtml
        htmlhint-ng2 www/**/*.{htm,html}

2. results

           test.html
              L5 |    </head>
                      ^ <title> must be present in <head> tag. (title-require)
              L8 |    </body>
                      ^ Tag must be paired, missing: [ </div> ], start tag match failed [ <div> ] on line 7. (tag-pair)

        2 errors in 1 files

3. config rules

    search `.htmlhintrc` file in current directory and all parent directories:

        htmlhint
        htmlhint test.html

    custom config file:

        htmlhint --config htmlhint.conf test.html

    custom rules:

        htmlhint --rules tag-pair,id-class-value=underline test.html

    Inline rules in `test.html`:

        <!--htmlhint tag-pair,id-class-value:underline -->
        <html>
        <head>
            ...

License
================

HTMLHint-ng2 is released under the MIT license:

> The MIT License
>
> Copyright (c) 2014-2015 Yanis Wang \< yanis.wang@gmail.com \>
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in
> all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
> THE SOFTWARE.

Thanks
================

* HTMLhint: [https://github.com/yaniswang/HTMLHint](https://github.com/yaniswang/HTMLHint)
* mocha: [https://github.com/visionmedia/mocha](https://github.com/visionmedia/mocha)
* expect.js: [https://github.com/LearnBoost/expect.js](https://github.com/LearnBoost/expect.js)
* istanbul: [https://github.com/gotwarlost/istanbul](https://github.com/gotwarlost/istanbul)
* Grunt: [http://gruntjs.com/](http://gruntjs.com/)
* commander.js: [https://github.com/visionmedia/commander.js](https://github.com/visionmedia/commander.js)
* colors.js: [https://github.com/Marak/colors.js](https://github.com/Marak/colors.js)
* glob: [https://github.com/isaacs/node-glob](https://github.com/isaacs/node-glob)
* jshint: [https://github.com/jshint/jshint](https://github.com/jshint/jshint)
* csslint: [https://github.com/stubbornella/csslint](https://github.com/stubbornella/csslint)
* GitHub: [https://github.com/](https://github.com/)
