# particles.js

[![Build Status](https://travis-ci.org/marcbruederlin/particles.js.svg?branch=master)](https://travis-ci.org/marcbruederlin/particles.js) [![dependencies Status](https://david-dm.org/marcbruederlin/particles.js/status.svg)](https://david-dm.org/marcbruederlin/particles.js) [![devDependencies Status](https://david-dm.org/marcbruederlin/particles.js/dev-status.svg)](https://david-dm.org/marcbruederlin/particles.js?type=dev) [![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)   

particles.js is a lightweight, dependency-free and responsive javascript plugin for particle backgrounds.

[<img src="http://i.giphy.com/CPEar2kArhFny.gif"/>](https://marcbruederlin.github.io/particles.js/)

## Installation
There are several ways to install particles.js:
- [Download the latest version](https://github.com/marcbruederlin/particles.js/archive/master.zip)
- Install with npm: `npm install particlesjs --save`
- Use the CDN: `https://npmcdn.com/particlesjs@2.0.0/dist/particles.min.js`

## Usage
Include the minified JS in your HTML (right before the closing body tag).
```html
<body>
  …
  <script src="path/to/particles.min.js"></script>
</body>
```

Add a canvas element to your markup (it should be the last element)
```html
<body>
  …
  <canvas class="background"></canvas>
  <script src="path/to/particles.min.js"></script>
</body>
```

Add a few styles to your css.
```css
html,
body {
  margin: 0;
  padding: 0;
}

.background {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 0;
}
```

Initialize the plugin on the `window.onload` event.
```js
window.onload = function() {
  Particles.init({
    selector: '.background'
  });
};
```

## Options
Option | Type | Default | Description
------ | ------------- | ------------- | -----------
`selector` | string | - | *Required:* The CSS selector of your canvas element
`maxParticles` | integer | `100` | *Optional:* Maximum amount of particles
`sizeVariations` | integer | `3` | *Optional:* Amount of size variations
`speed` | integer | `0.5` | *Optional:* Movement speed of the particles
`color` | string | `#000000` | *Optional:* Color of particles and connecting lines
`minDistance` | integer | `120` | *Optional:* Distance in `px` for conntecting lines
`connectParticles` | boolean | `false` | *Optional:* `true`/`false` if connecting lines should be drawn
`responsive` | array | `null` | *Optional:* Array of objects containing breakpoints and options

Example how to use the [responsive option](https://marcbruederlin.github.io/particles.js/#responsive-option).

## Browser Support
IE9+ and all modern browsers.

## Build
To compile the distribution files by yourself, make sure that you have node.js and gulp installed, then:
- Clone the repository: `https://github.com/marcbruederlin/particles.js.git`
- Change in the project directory: `cd particles.js`
- Install the dependencies: `npm install`
- Run the gulp build task `gulp build` to regenerate the `dist` folder. <br/> You can also run `gulp build --watch` to watch for file changes and automatically rebuild the files.

## Using particles.js?
If you’re using particles.js in some interesting way or on a cool site, I’d be very grateful if you <a href="mailto:hello@marcbruederlin.com?subject=Hey, I'm using particles.js">shoot me</a> a link to it.<br />
For any problems or questions don't hesitate to open an issue.<br />

## License
particles.js is created by [Marc Brüderlin](https://marcbruederlin.com) and released 
under the [MIT license](https://github.com/marcbruederlin/particles.js/blob/master/LICENSE).

## Version 1.x
The source code for particles.js 1.x has been moved to the [v1 branch](https://github.com/marcbruederlin/particles.js/tree/v1).
