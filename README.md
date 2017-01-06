<p align="center">
<img src="https://rdbrck.com/github/boilerbrck_v2.svg">
</p>

<h1 align="center">Rdbrck kit to start a new html/js project</h1>

### Features
- A lightweight batch of [HTML5 Boilerplate](https://html5boilerplate.com) features
- [.htaccess](.htaccess)
- Browser warning on IE9 or lower
- Polyfills for IE8 and below a la :heart: [ie-love](https://github.com/corysimmons/ie-love)
  - Conditionally loaded so only IE8 and below users will have to download it.
  - [html5shiv](https://github.com/aFarkas/html5shiv)
  - [calc-polyfill](https://github.com/closingtag/calc-polyfill)
  - [jQuery 1.x.x](https://jquery.com/download/)
  - [Selectivizr 2](https://github.com/corysimmons/selectivizr2)
  - [Respond.js](https://github.com/scottjehl/Respond)
- `.gitignore` for Node, Bower, and Sass

### Browser support

* Chrome *(latest 2)*
* Edge *(latest 2)*
* Firefox *(latest 2)*
* Internet Explorer 9+ (but generally IE8 should work fine with included [ie-love](https://github.com/corysimmons/ie-love) and [autoprefixer](https://github.com/postcss/autoprefixer))
* Opera *(latest 2)*
* Safari *(latest 2)*


### Installation

<p>1. Install <a href="https://nodejs.org/en/">nodejs</a> with npm</p>
<p>2. Install bower globally</p>
```sh
npm install -g bower
```
<p>3. Install gulp globally</p>
```sh
npm install --global gulp-cli
```
<p>4. Run gulp inside project directory</p>
```sh
gulp
```



## Included tools

#### Lost Grid
Powerful grid system built in PostCSS. By default, template has flexbox support disabled by default to support IE9.

##### Why not bootstrap?
Bootstrap is fine, but not enough. Large css file with lot of mess, fixed breakpoints, fixed layout to 12 columns. In Grid you can define fixed gutters. Everything is described in [docs](http://lostgrid.org/docs.html). Recently author of that plugin started to work on [video tutorials](https://www.youtube.com/watch?v=6FN7QU1ZxqA&list=PLHYmM0rBloyTelftsYtk93VgunoYmNkc5)

#### Gulp packages / PostCSS plugins
- [autoprefixer](https://github.com/postcss/autoprefixer) - handles css prefixes automatically
- [postcss-filter-gradient](https://github.com/yuezk/postcss-filter-gradient) - plugin for generating the old IE supported filter gradient.
- [postcss-opacity](https://github.com/iamvdo/postcss-opacity) - plugin that adds support for legacy browser opacity alternatives.
- [PreCSS](https://github.com/jonathantneal/precss) - tool that allows you to use Sass-like markup in your CSS files.
- [gulp-uglify](https://github.com/terinjokes/gulp-uglify) - UglifyJS
- [gulp-minify-css](https://www.npmjs.com/package/gulp-minify-css) - minifies CSS
- [gulp-concat](https://www.npmjs.com/package/gulp-concat) - concatenates files
- [cssnext](http://cssnext.io/) - transforms new CSS specs into more compatible CSS
- [browser-sync](https://www.browsersync.io/) - synchronized browser testing

#### Js Libraries

