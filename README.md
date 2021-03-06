<p>
  <a href="https://travis-ci.org/KitchenStories/vue-gallery-slideshow"><img src="https://img.shields.io/travis/KitchenStories/vue-gallery-slideshow.svg?style=flat-square"></a>
  <a href="https://www.npmjs.com/package/vue-gallery-slideshow"><img src="https://img.shields.io/npm/dt/vue-gallery-slideshow.svg?style=flat-square"></a>
</p>  

# vue-gallery-slideshow

![](https://github.com/KitchenStories/vue-gallery-slideshow/blob/master/images/demo.gif)

## Live Demo
[https://jsfiddle.net/headione/szk73x45/3/](https://jsfiddle.net/headione/szk73x45/3/)

## Installation

#### NPM

```bash
npm install vue-gallery-slideshow --save
```

## Usage

#### HTML

```html
<div id="app">
  <img class="image" v-for="(image, i) in images" :src="image" @click="onClick(i)">
  <vue-gallery-slideshow :images="images" :index="index" @close="index = null"></vue-gallery-slideshow>
</div>
```


#### JavaScript

```javascript
import VueGallerySlideshow from 'vue-gallery-slideshow'


const app = new Vue({
  el: '#app',
  components: {
    VueGallerySlideshow
  },
  methods: {
    onClick(i) {
      this.index = i;
    }
  },
  data: {
    images: [
      'https://placekitten.com/801/800',
      'https://placekitten.com/802/800',
      'https://placekitten.com/803/800',
      'https://placekitten.com/804/800',
      'https://placekitten.com/805/800',
      'https://placekitten.com/806/800',
      'https://placekitten.com/807/800',
      'https://placekitten.com/808/800',
      'https://placekitten.com/809/800',
      'https://placekitten.com/810/800'
    ],
    index: 0
  }
})

```

## Contributing

Please refer to each project's style guidelines and guidelines for submitting patches and additions. In general, we follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

## Author

Norman Sander, norman@nsander.de

## License

vue-gallery-slideshow is available under the MIT license. See the LICENSE file for more info.
