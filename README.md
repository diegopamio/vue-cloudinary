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

```

(*) See [cloudinary documentation](http://cloudinary.com/documentation/rails_additional_topics#configuration_options) for a complete list of the options available. 

index.html
```html
<div id="example1">
    <img v-cl-image="my_logo" width="auto" responsive fetch_format="auto" quality="auto"></p>
</div>
```
Further image manipulation options are listed in [this reference](http://cloudinary.com/documentation/image_transformations#reference).

Note that the attribute names in the docs are using snake_case, however this SDK supports both snake_case and kebab-case for attribute names, e.g. both fetch_format: 'auto' and 'fetch-format': 'auto' are eventually translated to f_auto.
## License

[MIT](https://opensource.org/licenses/MIT)
