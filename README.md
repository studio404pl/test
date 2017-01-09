<p align="center">
<img src="https://rdbrck.com/github/boilerbrck_logo.svg">
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
Bootstrap is fine, but it's not enough. Large css file with lot of mess, fixed breakpoints, fixed layout to 12 columns. In Lost Grid you can define fixed gutters, different grid layouts, define cycles, control shifts etc. Everything is described in [docs](http://lostgrid.org/docs.html). Recently author of that plugin started to work on [video tutorials](https://www.youtube.com/watch?v=6FN7QU1ZxqA&list=PLHYmM0rBloyTelftsYtk93VgunoYmNkc5)

#### Gulp packages / PostCSS plugins
- [PreCSS](https://github.com/jonathantneal/precss) - tool that allows you to use Sass-like markup in your CSS files.
- [cssnext (includes autoprefixer)](http://cssnext.io/) - transforms new CSS specs into more compatible CSS
- [postcss-filter-gradient](https://github.com/yuezk/postcss-filter-gradient) - plugin for generating the old IE supported filter gradient.
- [postcss-opacity](https://github.com/iamvdo/postcss-opacity) - plugin that adds support for legacy browser opacity alternatives.
- [gulp-uglify](https://github.com/terinjokes/gulp-uglify) - UglifyJS
- [gulp-minify-css](https://www.npmjs.com/package/gulp-clean-css) - minifies CSS with clean-css
- [gulp-concat](https://www.npmjs.com/package/gulp-concat) - concatenates files
- [browser-sync](https://www.browsersync.io/) - synchronized browser testing
- [gulp-real-favicon](https://www.npmjs.com/package/gulp-real-favicon) - favicon generator. [Jump to section](#favicon-generator)
- [gulp-imagemin](https://github.com/sindresorhus/gulp-imagemin) - image optimization. [Jump to section](#image-optimization)

#### js libraries
- [lightcase](http://cornel.bopp-art.com/lightcase/) - lightweight and beautiful lightbox with lot of options and support different content. Unfortunately it's based on jQuery. If you know similar library but without dependencies - please let me know.
- [remodal](https://github.com/VodkaBears/Remodal) - responsive, lightweight, fast, synchronized with CSS animations, fully customizable modal window plugin with declarative configuration and hash tracking. No dependencies.
- [retinajs](https://github.com/imulus/retinajs) - supports retina images, included in js and sass already. No dependencies.
- [scrollreveal](https://github.com/jlmakes/scrollreveal) - lightweight and simple animation library. No dependencies.
- [slick](http://kenwheeler.github.io/slick/) - simple and powerfull tool for slider modules and carousels. No dependencies.

All above libraries are optional and kit supports them. You can include them easily just by declaring true/false value next to library name in `gulpfile.js` at the very top. Everything else (including js/css files, concatenating) is handled automatically.



#### favicon generator

To easily generate favicon images in all formats you just have to replace source file (minimum 260x260 pixels):

```sh
assets/images/favicon_src.png
```

and run command that will generate all favicons related files:

```sh
gulp generate-favicon
```

to inject necessary code into header section of main template file you just have to run:

```sh
gulp inject-favicon-markups
```

and you are ready to roll.

You can adjust background colors, application name etc. in `gulpfile.js`



#### image optimization

Place all your original image files in:

```sh
assets/images/org/
```

and run:

```sh
gulp images
```

optimized version of all images will be saved in `assets/images/` directory.

## Additional information

#### structure

- page content should be placed in `pagename_content.php` file. You can display page content by adding in kit url parameter `page`.
```sh
?page=pagename
```
`main` is default value.
- all assets should be placed in `assets` directory,
- all assets *has to be* loaded from assets directory. Do not link to `bower_components` directory in any case.
- all libraries should be installed via package managers (bower or npm),
- try to separate css styling to different layouts and modules files ie.
```sh
@import 'layouts/header';
@import 'layouts/footer';

@import 'layouts/form';

@import 'layouts/main';
@import 'layouts/single';
@import 'layouts/contact';
```

## FAQ

That section will be filled out in near future. You can also create an issue if you have question or new idea for extending kit or modifying some things.

#### what about icons?

##### By icons i mean situation when i have more than 10 images and want to use them in different sizes and places.

##### For solid (one color) icons i recommend [fontello - fontface generator](http://fontello.com). It supports literally all platforms. You can review uploaded icons, download export file for future use, style sizes and colors through css.

##### For multiple colors i recommend [grumpicon](http://www.grumpicon.com/) it's a webapp wrapper for grunticon that handles all necessary processes and generate for you all svg images with png fallbacks and stylesheets.

##### Of course you can go with svg's 

## CHECKLIST before pushing project to acceptation

- if you are using retinajs plugin and don't have retina device you have to test it on your own. Place below code in head section to spoof retina device:

```javascript
<script type="text/javascript">
  // Spoof the browser into thinking it is Retina
  // comment the next line out to make sure it works without retina
  window.devicePixelRatio = 2;
</script>
```

and check developer console against any 404 errors for image files.

- check your project on [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) - you should get mobile score larger than 70 and for desktops it should be more than 85.

- check your project on [GTmetrix](https://gtmetrix.com) - it should be at least A grade for PageSpeed and YSlow (~90%)
