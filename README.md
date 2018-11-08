
# svg-to-vue-component

[![NPM version](https://badgen.net/npm/v/svg-to-vue-component)](https://npmjs.com/package/svg-to-vue-component) [![NPM downloads](https://badgen.net/npm/dm/svg-to-vue-component)](https://npmjs.com/package/svg-to-vue-component) [![CircleCI](https://badgen.net/circleci/github/egoist/svg-to-vue-component/master)](https://circleci.com/gh/egoist/svg-to-vue-component/tree/master)  [![donate](https://badgen.net/badge/support%20me/donate/ff69b4)](https://patreon.com/egoist) [![chat](https://badgen.net/badge/chat%20on/discord/7289DA)](https://chat.egoist.moe)

## Install

```bash
yarn add svg-to-vue-component --dev
```

## Usage

### With Webpack

```js
// webpack.config.js
module.exports = {
  module: {
    rules: [
      {
        test: /\.svg$/,
        use: [
          // This loader compiles .svg file to .vue file
          // So we use `vue-loader` after it
          'vue-loader',
          'svg-to-vue-component/loader'
        ]
      }
    ]
  },
  // ...other configurations
}
```

Then you can import `.svg` files directly and use them as Vue functional components:

```vue
<template>
  <!-- Dom props and events are all available here -->
  <CheckIcon width="20px" height="20px" @click="handleClick" />
</template>

<script>
import CheckIcon from './check-icon.svg'

export default {
  components: {
    CheckIcon
  },

  methods: {
    handleClick() {
      console.log('It works!')
    }
  }
}
</script>
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## Author

**svg-to-vue-component** © [EGOIST](https://github.com/egoist), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by EGOIST with help from contributors ([list](https://github.com/egoist/svg-to-vue-component/contributors)).

> [Website](https://egoist.sh) · GitHub [@EGOIST](https://github.com/egoist) · Twitter [@_egoistlily](https://twitter.com/_egoistlily)