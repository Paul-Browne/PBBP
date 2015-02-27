## BoilerPlate +

#####Ok. So Whats the plus?

Basically it adds

1. Responsive image replacement
2. Better &lt;img&gt; control
3. Full screen containers
4. Vertically centered elements
5. Scalable typography
6. Stopping FOUC and page yank
7. A simple Grid System
8. Better fonts, inc an icon font

[DEMO](https://rawgit.com/Paul-Browne/PBBP/master/index.html)

#### 1. Responsive Image Replacement

[A simple script](https://github.com/Paul-Browne/responsive-images.js) that swaps out images depending on the width of the image's *container* and the device's pixel ratio.
You can specify as many, or as few breakpoints as you like. The placeholder image should be of sufficient size ie. 1024x768, but of low quality ~ 20kb. Having a placeholder image is optional.

```html
<div class="container"> // optional, could just be the <body>
  <img src = "i/world-placeholder.jpg" class="foo" id="bar" alt=""
  data-src = "<400:i/world-small.jpg,
              <800:i/world-medium.jpg,
              <1200:i/world-large.jpg,
              <1600:i/world-huge.jpg,
              >1600:i/world-massive.jpg" />
</div>
```

So, in the above example (assuming the `container` was the full screen);

On a regular laptop - screen size = `1366px`, device pixel ratio = `1`. Image displayed = `world-huge`.
On a Samsung galaxy S4 (landscape) - screen size = `640px`, device pixel ratio = `3`. Image displayed = `world-massive`.
On an iphone 3GS (portrait) - screen size = `320px`, device pixel ratio = `1`. Image displayed = `world-small`.
On an iphone 4S (portrait) - screen size = `320px`, device pixel ratio = `2`. Image displayed = `world-medium`.



#### 2. Image Cover

[A simple script](http://paulbrowne.fi/2015/01/31/background-image-properties-inline-images) that mimics `background-size:cover; background-position:center center;` on `<img>` elements.
Just wrap your `<img>` in a container with the class `icovr` like so;

```html
<div class="icovr" id="bar">
  <img src="i/a-picture.jpg" alt="" />
</div>
```

Will also work with responsive images. The container should have a height specified.

#### 3. Full Screen Containers

[A simple script](http://paulbrowne.fi/2015/01/22/full-width-full-height-full-screen-helper-plugin) that allows you to add a container that will have the same dimensions (height and width) as the viewport.

```html
<div class="fullscreen">
  // content
</div>
```

Use the class `fullheight` if you want to create a container with only the same height as the viewport.

#### 4. Middlize

[A simple script](http://paulbrowne.fi/2014/12/04/vertically-center-element) that allows you to vertically and horizontally center any element within It's container.

```html
<div class="container">
  <div class="middlize"><h1>Hello World!</h1></div>
</div>
```

To only vertically center the element use the class `vmid` instead. The container should have a height specified.

#### 5. Scalable Typography

[A simple script](https://github.com/Paul-Browne/typeScale) that tweeks the base font size and line-height depending on the width of the viewport (browser window).

#### 6. FOUC and Page Yank

[A simple script](https://github.com/Paul-Browne/FOUC-and-Page-Yank) that hides the page whilst its loading, then has it fade in when ready and fade out when navigated away from or refreshed.

#### 7. A Simple Grid System

[A simple script](https://github.com/Paul-Browne/epicGrid)

add content here

#### 8. Fonts via google and icomoon

[Open Sans and libre baskerville](https://www.google.com/fonts/#UsePlace:use/Collection:Libre+Baskerville:400italic|Open+Sans:400,600) via google fonts. Open Sans - 400 is used for the main body text, Open Sans - 600 for bold/strong text and headlines (h1 - h6). Libre Baskerville - 400 italic is used for blockquotes, addresses, emphasis and anything else that requires italics.

The iconfont was generated using [icomoon](https://icomoon.io/) It includes a whole bunch of commonly used symbols


