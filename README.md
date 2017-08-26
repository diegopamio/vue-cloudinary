# vue-cloudinary

> A [Vue.js](https://github.com/vuejs/vue) plugin that offers a reusable directive to get image from [cloudinary](https://cloudinary.com)

[![npm version](https://img.shields.io/npm/v/vue-cloudinary.svg)](https://www.npmjs.com/package/vue-cloudinary)

## Overview

This is a port of the angular-cloudinary library to VueJS.

## Use cases

- Show image from cloudinary

## Requirements

- vue: ^2.0.0

If you need a version for Vue 1, sorry, you'll need to do your own.

## Install

From npm:

``` sh
$ npm install vue-cloudinary --save
```

## Usage

app.js:
``` javascript
    
Vue.use(VueCloudinary, {
  "cloud_name": "<your cloud name>",
  "api_key": "<your api key>",
  "cdn_subdomain": true,
  ... (*)
});

new Vue({
  el: '#example1',
  data: {
    shown: true,
    exampleImage1: {
        publicId: 'lg82vjkqbg9f3fzrqem6'
    }
  },
});

```

index.html
```html
<div id="example1">
    <img v-cl-image="exampleImage1"></p>
</div>
```

(*) See [cloudinary documentation](http://cloudinary.com/documentation/rails_additional_topics#configuration_options) for a complete list of the options available. 

## License

[MIT](https://opensource.org/licenses/MIT)
