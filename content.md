<img class="stretch" data-src="media/img/aframe-logo-rendered.png">

# A-Frame

## Building Blocks for the VR Web

Ram / Mozilla India Meetup 2016

------

# Virtual Reality (VR)

Technology that simulates physical presence in interactive and realistic 3D
environments

<!--Notes
- Next platform. From PCs -> Smartphones -> VR
- Change how we work + play + communicate digitally
-->

---

## Hardware

<div class="image-row">
  <div><img data-src="media/img/google-cardboard.png"></div>
  <div><img data-src="media/img/google-daydream.png"></div>
  <div><img data-src="media/img/samsung-gearvr.png"></div>
</div>

<div class="image-row">
  <div><img data-src="media/img/oculus-rift.png"></div>
  <div><img data-src="media/img/playstation-vr.png"></div>
  <div><img data-src="media/img/htc-vive.png"></div>
</div>

<!--Notes
- Range from free to $899
- Tethered and untethered
- Powered by smartphone, gaming consoles, and PCs
-->

---

## Friction of VR Ecosystems

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/gatekeeper.png">
    <i>Gatekeepers</i>
  </div>
  <div>
    <img data-src="media/img/downloads-installs.png">
    <i>Installs</i>
  </div>
  <div>
    <img data-src="media/img/closed-door.png">
    <i>Closed</i>
  </div>
</div>

<!--Notes
- Gatekeepers: app stores control approval/distribution, can take down content,
  single points of failure
- Installs: users have to go through downloads/installs
- Closed: proprietary tech (Unity/Unreal), steep learning curve, fragmented
  causes cross-compat issues, siloed experiences
-->

------

# WebVR

An open virtual reality platform with the advantages of the Web

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/web-is-open.png">
    <i>Open</i>
  </div>
  <div>
    <img data-src="media/img/web-is-connected.png">
    <i>Connected</i>
  </div>
  <div>
    <img data-src="media/img/web-is-instant.png">
    <i>Instant</i>
  </div>
</div>

<!--Notes
- Open: anyone can publish, open source, open standards
- Connected: traverse from world to world, not siloed experiences
- Instant: click a link, immediately get into an experience, easily sharable via links
-->

---

<img class="stretch" data-src="media/img/webvr.png">

**Standard browser APIs** that enable **WebGL rendering to headsets** and
**access to VR sensors**.
https://w3c.github.io/webvr/

<!--Notes
- Working W3C community group
- Initial WebVR API by Mozilla (Vlad V.)
- Mozilla, Google, Samsung, Microsoft, community currently drafting WebVR 1.0 API
- .Optimized rendering path to headsets, 90fps+
- .Access position and rotation (pose) data
-->

---

## Browser Support

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/firefox-nightly.png">
    <i>Firefox Nightly</i>
  </div>
  <div>
    <img data-src="media/img/chromium.png">
    <i>Chromium (Experimental)</i>
  </div>
  <div>
    <img data-src="media/img/samsung-browser.png">
    <i>Samsung Internet</i>
  </div>
  <div>
    <img data-src="media/img/google-cardboard.png">
    <i>Mobile Polyfill</i>
  </div>
</div>

<!--Notes
- Firefox + Chrome WebVR 1.0 hits release channels by early 2017
- Firefox Nightly: first WebVR browser
- Chromium: custom Chromium builds by Brandon Jones
- Samsung: GearVR browser, with a flag
- Mobile Polyfill: use device motion/orientation sensors to polyfill on smartphones
-->

------

# A-Frame

A web framework for building virtual reality experiences with HTML

```html
<a-scene>
  <a-box color="#4CC3D9" position="-1 0.5 -3" rotation="0 45 0"></a-box>
  <a-cylinder color="#FFC65D" position="1 0.75 -3" radius="0.5" height="1.5"></a-cylinder>
  <a-sphere color="#EF2D5E" position="0 1.25 -5" radius="1.25"></a-sphere>
  <a-plane color="#7BC8A4" rotation="-90 0 0" position="0 0 -4" width="4" height="4"></a-plane>
  <a-sky color="#ECECEC"></a-sky>
</a-scene>
```

<!--Notes
- Launched December 2015 by the Mozilla VR team
- Make it easy for anyone to create VR content
- Enable web developers
- Prototype and experiment faster
- Kickstart WebVR ecosystem
- Tag names representing objects, customize with attributes
-->

---

## Supports Anything w/ WebVR

<div class="image-row">
  <div><img data-src="media/img/google-cardboard.png"></div>
  <div><img data-src="media/img/samsung-gearvr.png"></div>
  <div><img data-src="media/img/oculus-rift.png"></div>
  <div><img data-src="media/img/htc-vive.png"></div>
</div>

<div class="image-row">
  <div><img data-src="media/img/firefox-nightly.png"></div>
  <div><img data-src="media/img/chromium.png"></div>
  <div><img data-src="media/img/samsung-browser.png"></div>
  <div><img data-src="media/img/google-cardboard.png"></div>
</div>

<!--Notes
- Like the Web, works most everywhere, currently WebVR 1.0 API
- Even supports HTC Vive + tracked controllers (experimental Gamepad API)
- Mobile browsers (polyfill), although accessible, have tons of issues
-->

---

## Hello World

<div data-aframe-scene="scenes/hello-world.html"></div>

<!--Notes
- It's the web, we can embed VR in HTML slide
- It's the web, view source in DOM inspector and change values live
- Click-drag to rotate the camera
- Can go fullscreen, would go into VR if a headset was connected
- Can view on mobile if people go to aframe.io
-->

---

## With MagicaVoxel

<img data-src="media/img/magicavoxel.png">

<!--Notes
- Can create scenes with MagicaVoxel
- Super easy tool, drop blocks like Minecraft
- Then export to A-Frame
-->

---


# Why A-Frame?

- **Simple** &mdash; zero boilerplate
- **Easy** &mdash; use with languages and tools we know
- **Powerful** &mdash; declarative entity-component-system

<!--Notes
-->

------

## Boilerplate without A-Frame

<!-- .slide: data-background-video="media/video/boilerplate.mp4" data-state="background-low-opacity" data-transition="concave" data-background-transition="none" -->

<div class="slide__boilerplate">
  <p>Import WebVR polyfill</p>
  <p>Set up camera</p>
  <p>Set up lights</p>
  <p>Initialize scene</p>
  <p>Declare and pass canvas</p>
  <p>Listen to window resize</p>
  <p>Install VREffect</p>
  <p>Instantiate renderer</p>
  <p>Create render loop</p>
  <p>Preload assets</p>
  <p>Figure out responsiveness</p>
  <p>Deal with metatags and mobile</p>
</div>

<!--Notes
-->

---

<!-- .slide: data-transition="concave" -->

```html
<a-scene></a-scene>
```

<!--Notes
-->

---

## The Simplest Things Made Simpler

<!-- .slide: data-transition="concave" -->

```js
// Box in three.js
var geometry = new THREE.BoxGeometry(1, 2, 3);
var material = new THREE.MeshStandardMaterial({color: 'red'});
var box = new THREE.Mesh(geometry, material);
box.position.set(10, 0, 10);
scene.add(box);
```

<!--Notes
-->

---

<!-- .slide: data-transition="concave" -->

```html
<a-box color="red" position="10 0 10"></a-box>
```

<!--Notes
-->

------

## Languages & Tools We Know

- HTML
- JavaScript and DOM APIs
- Integrates with existing frameworks and libraries

```js
var scene = document.querySelector('a-scene');
var sphere = document.createElement('a-sphere');
sphere.setAttribute('radius', 2);
scene.appendChild(sphere);
```

<!--Notes
-->

---

## Languages & Tools We Know

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/d3.png">
    <i>d3.js</i>
  </div>
  <div>
    <img data-src="media/img/vue.png">
    <i>vue.js</i>
  </div>
  <div>
    <img data-src="media/img/react.png">
    <i>React & Redux</i>
  </div>
</div>

<!--Notes
-->

---

## Languages & Tools We Know

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/magicavoxel.png">
    <i>MagicaVoxel</i>
  </div>
  <div>
    <img data-src="media/img/blender.png">
    <i>Blender</i>
  </div>
  <div>
    <img data-src="media/img/maya.png">
    <i>Maya</i>
  </div>
</div>

<!--Notes
-->

------

# Entity-Component-System

<img class="stretch" data-src="media/img/entity-component-system.png">

- Composable, reusable, sharable bits of code
- All the power of JavaScript, three.js, and WebGL
- Developers empower other developers

<!--Notes
-->

---

<!-- .slide: data-transition="slide-in none" -->

## Composing an Entity

```html
<a-entity></a-entity>
```

<!--Notes
-->

---

<!-- .slide: data-transition="none" -->

## Composing an Entity

```html
<a-entity geometry="primitive: plane; height: 10000; width: 10000">
```

<!--Notes
-->

---

<!-- .slide: data-transition="none" -->

## Composing an Entity

```html
<a-entity geometry="primitive: plane; height: 10000; width: 10000"
          rotation="-90 0 0">
```

<!--Notes
-->

---

<!-- .slide: data-transition="none" -->

## Composing an Entity

```html
<a-entity geometry="primitive: plane; height: 10000; width: 10000"
          rotation="-90 0 0"
          material="shader: standard; opacity: 0.8">
```

<!--Notes
-->

---

## Composing an Entity

<!-- .slide: data-transition="none" -->

```html
<a-entity geometry="primitive: plane; height: 10000; width: 10000"
          rotation="-90 0 0"
          material="shader: standard; normalTextureRepeat: 50 50; opacity: 0.8"
          ocean-waves="intensity: 0.7">
```

<!--Notes
-->

---

## Baking an Entity

```js
AFRAME.registerPrimitive('a-ocean', {
  defaultComponents: {
    'ocean-waves': {intensity: 0.7}
  },

  mappings: {
    'reflection': 'material.sphericalEnvMap',
    'wave-intensity': 'ocean-waves.intensity'
  }
});
```

```html
<a-ocean reflection="url(sky.png)" wave-intensity="2"></a-ocean>
```

<!--Notes
-->

---

## Structure of a Component

```js
AFRAME.registerComponent('position', {
  schema: {type: 'vec3'},

  update: function () {
    var el = this.el;  // Reference to the entity element.
    var data = this.data;  // Component data parsed from HTML.
    var object3D = el.object3D;  // three.js Object.

    object3D.position.set(data.x, data.y, data.z);
  }
});
```

<!--Notes
-->

---

## Writing a Component

```js
AFRAME.registerComponent('crazy-position', {
  schema: {
    min: {type: 'vec3'},
    max: {type: 'vec3'}
  },

  tick: function () {
    var data = this.data;
    var randomPosition = __getRandomPosition(min, max);
    this.el.object3D.position.copy(randomPosition);
  }
});
```

```html
<a-sphere crazy-position="min: -1 -1 -1; max: 1 1 1"></a-sphere>
```

<!--Notes
-->

------

# Community

- **Github**: 60 contributors, 2800 stargazers
- **Slack**: 1300 members
- **Content**: Hundreds of projects featured on `awesome-aframe` repository and *A Week of A-Frame*
- **Stackoverflow**: Q & A
- **Recognition**: A Week of A-Frame

<!--Notes
-->

---

<!-- .slide: data-background="media/img/standard-components.png" data-background-size="contain" -->

<!--Notes
-->

---

<!-- .slide: data-background="media/img/community-components.png" data-background-size="contain" -->

<!--Notes
-->

------

# Augmented Reality

<video class="stretch" data-src="media/video/argon.mp4" data-autoplay loop></video>

<!--Notes
-->

------

<!-- .slide: data-background="media/img/scene-collage.jpg" data-state="background-low-opacity" style="background-color: rgba(239, 45, 94, 0.9); color: #EEE" -->

# Questions?  <!-- .element: style="color: #FFF" -->

- Try it out [aframe.io](https://aframe.io)
- Join us on Slack [aframevr-slack.herokuapp.com](https://aframevr-slack.herokuapp.com/)
- Follow us [@aframevr](https://twitter.com/aframevr)
- Ram | [@ram_gurumukhi](https://twitter.com/ram_gurumukhi)

<!--Notes
-->
