# vue3-picker-emoji
____

A new emoji / gif picker for your app !

This components is available only in vue3.

🚧 Rework in typescript and composition-api soon.

### Install
```js
npm install vue3-picker-emoji
```

### Global
```js
import Vue from 'vue'
import PickerEmoki from 'vue3-picker-emoji'

Vue.use(PickerEmoki, /* { default options with global component } */)
```

### Local registration
```js
import PickerEmoki from 'vue3-picker-emoji'

export default {
  components: {
    PickerEmoki
  }
}
```

____

## Props
| Name   |      Type      |  Default | Description |
|----------|:-------------:|:------:|------:|
| input |    `Boolean`   |   false |  Load input w/ autocomplete |
| value | `String`, `Number` |  null | v-model to input value |
| categories | `Array` |   true | Display the mask on first load |
| gifFormat | `String` |  | Return gif link with markdown format or html format (default: nothing) |
| apiKey | `String` |  | API_KEY tenor.com (free, register here: https://tenor.com/gifapi) (if no key: gif not appear) |
| showUpload | `Boolean` |  | Display upload icon at left (with emit method) |
| showEmoji | `Boolean` |  | Display emoji icon |
| sources | `Object` |  | Set new source url for all image |

### Sources props
"search": `String`
"gif": `String`
"emoji": `String`
"category": `String` (add %REPLACE% in your URL to change with slug, example: `/categories/%REPLACE%.svg` transform into /categories/animals.svg`)
"variation": `String` (same at category, example: `/variations/variation_%REPLACE%.svg` transform into `/variations/variation_0.svg` (0 - 4))

### Categories
All categories list:
`['people', 'animals', 'foods', 'travel', 'activities', 'objects', 'symbols', 'flags']`

