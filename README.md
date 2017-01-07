<p align="center">
<img src="https://rdbrck.com/github/boilerbrck.svg?n=1">
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
<p>4. Install npm packages inside project directory</p>
```sh
npm install
```
<p>5. Install bower packages inside project directory</p>
```sh
bower install
```
<p>6. Run gulp inside project directory</p>
```sh
gulp
```



## Included tools

#### Lost Grid
Powerful grid system built in PostCSS. By default, template has flexbox support disabled to support IE9.

##### Why not bootstrap?
Bootstrap is fine, but it's not enough. Large css file with lot of mess, fixed breakpoints, fixed layout to 12 columns. In Grid you can define fixed gutters, different grid layouts, define cycles, control shifts etc. Everything is described in [docs](http://lostgrid.org/docs.html). Recently author of that plugin started to work on [video tutorials](https://www.youtube.com/watch?v=6FN7QU1ZxqA&list=PLHYmM0rBloyTelftsYtk93VgunoYmNkc5)

#### Gulp packages / PostCSS plugins
- [PreCSS](https://github.com/jonathantneal/precss) - tool that allows you to use Sass-like markup in your CSS files.
- [cssnext (includes autoprefixer)](http://cssnext.io/) - transforms new CSS specs into more compatible CSS
- [postcss-filter-gradient](https://github.com/yuezk/postcss-filter-gradient) - plugin for generating the old IE supported filter gradient.
- [postcss-opacity](https://github.com/iamvdo/postcss-opacity) - plugin that adds support for legacy browser opacity alternatives.
- [gulp-uglify](https://github.com/terinjokes/gulp-uglify) - UglifyJS
- [gulp-minify-css](https://www.npmjs.com/package/gulp-clean-css) - minifies CSS with clean-css
- [gulp-concat](https://www.npmjs.com/package/gulp-concat) - concatenates files
- [browser-sync](https://www.browsersync.io/) - synchronized browser testing

#### js libraries
- [lightcase](http://cornel.bopp-art.com/lightcase/) - lightweight and beautiful lightbox with lot of options and support different content. Unfortunately it's based on jQuery. If you know similar library but without dependencies - please let me know.
- [retinajs](https://github.com/imulus/retinajs) - supports retina images, included in js and sass already, no dependencies
- [scrollreveal](https://github.com/jlmakes/scrollreveal) - lightweight and simple animation library, no dependencies
- [slick](http://kenwheeler.github.io/slick/) - simple and powerfull tool for slider modules and carousels, no dependencies

All above libraries are optional and kit supports them. You can include them easily just by declaring true/false value next to library name in `gulpfile.js`. Everything else (including js/css files, concatenating) is handled in gulp.

#### 
