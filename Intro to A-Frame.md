autoscale:true

# [fit] An Introduction
## [fit] To **A-Frame**
---

# [fit] It's **A Frame**work
# [fit] for easily working
# [fit] with **WebGL and VR**

---

# [fit] Use **markup** to create
# [fit] **VR experiences** that work
# [fit] across **desktop**, **iOS**
# [fit] **Android**, and **VR Headsets**

---

# [fit] Entity: an object
# [fit] `<a-entity>`

---

# [fit] Common entities
### `<a-box>`
### `<a-sphere>`
### `<a-plane>`
### `<a-obj-model>`
# [fit] **and many more...**

---

# [fit] Component: a property
# [fit] `<a-entity width="2">`

---
#<br>
# [fit] Common components:

# [fit] `width`, `height`, `depth`, `radius`
# [fit] `material`, `geometry`, `src`
# [fit] `id`, `position`, `rotation`
# [fit] **and many more...**

---

# [fit] Creating a **red box**

---

```html
<a-scene>
  <a-box
    color="red"
  ></a-box>
</a-scene>
```

---

# [fit] ... that's it!

---

![](http://i.imgur.com/jlbXvde.gif)

---

# [fit] Oh there's a bit more

---

# [fit] Sizing
# [fit] You can either use
# [fit] `width="2" height="2" depth="2"`
# [fit] or the **geometry** component:
# [fit] `geometry="width: 2; height: 2; depth: 2"`

---

# [fit] Scaling
# [fit] `scale="1 1 1"`
# [fit] Specified in terms of **x**, **y** and **z** axis
# [fit] Can use negative numbers to mirror on an axis

---

# [fit] Positioning
# [fit] `position="0 0 0"`
# [fit] Starts from **0 0 0** in your scene
# [fit] Specified in terms of **x**, **y** and **z** axis

---

# [fit] Materials
# [fit] The appearance of an entity
# [fit] `material="color: red; opacity: .5"`
# [fit] Used to define **color**, **opacity**
# [fit] **rendering effect** and texture **src**

---

# [fit] Lighting
# [fit] Cast light in your scene
# [fit] **Types:** ambient, directional
# [fit] hemisphere, point, spot
# [fit] Can also specify the color, intensity, angle

---

# [fit] Assets
# [fit] Used for preloading **textures**
# [fit] **sounds**, **videos**, and defining **mixins**

---

```html
<a-assets>
  <img id="texture1" src="texture.png" />
  <audio id="coin" src="coin.mp3"></audio>
  <video id="rick" src="nggyu.mp4"></video>
  <a-mixin id="massive" scale="10 10 10"></a-mixin>
</a-assets>
```

---

# [fit] Animating
# [fit] Specify the **attribute** to animate
# [fit] the state to go **from** and **to**, the **dur**
# [fit] of the animation, the **fill** mode, **repeat**
# [fit] count, **direction** and **easing** method.

---

```html
<a-entity ...>
  <a-animation
    attribute="rotation"
     dur="10000"
     fill="forwards"
     to="0 360 0"
     easing="linear"
     repeat="indefinite"
   ></a-animation>
</a-entity>
```

---

![](http://i.imgur.com/nyMXDjM.gif)

---

# [fit] Interaction
# [fit] Interact with entities through **clicking** or **gazing**

---

# [fit] Basically...
# [fit] when you **look at stuff**
# [fit] You can **make stuff happen**

---

# [fit] Read the A-Frame
# [fit] docs for **cursor**

---

# [fit] Manipulating
# [fit] things with
# [fit] **Javascript**

---

<br>
# [fit] Vanilla JavaScript

```javascript
.querySelector('a-image')
.getAttribute('opacity')
.setAttribute('material', 'color', 'red')
.addEventListener('collide')
.createElement('a-entity')
```

---


# [fit] With libraries...

```javascript
// jQuery
$('a-box').attr('width', 5);

// d3
d3.select('a-scene')
  .selectAll('a-box.bar')
  .data(data);
```

---

# [fit] If you hate writing
# [fit] HTML-**esque** markup

---

# [fit] Use a **templating** language!

```javascript
// Jade/Pug example
a-scene(
  fog='type: linear; far: 20; color: #1a1a1a'
)
  a-entity(
    position='2 2.5 0'
    rotation='0 12 0'
  )
    each foo,index in locals.bar
      a-entity(
        position=(index * 1.4) + ' 0 ' + (index * -2)
        rotation='0 ' + (index * -15) + ' 0'
      )
```

---

# [fit] A short guide
# [fit] **blog.omgmog.net/gdd-aframe-guide**

---

# [fit] Boilerplate
# [fit] **github.com/aframevr/aframe-boilerplate**

---

# [fit] Official docs
# [fit] **aframe.io/docs/0.2.0/guide**

---

# [fit] Some examples
# [fit] **aframe.io/aframe/examples**
