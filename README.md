# sample_vue-datepicker


## [1]. Nuxt Install

```
% npx nuxi init nuxt3-vue-datepicker
% cd nuxt3-vue-datepicker
% npm install
% npm run dev
```

http://localhost:3000 へアクセス、Nuxt3の実行を確認。



## [2]. vue-datepicker のインストール

```
% npm install @vuepic/vue-datepicker
```



## [3]. pages/index.vue に vue-datepicker を実装。

app.vue で pages/index.vue を表示するための改修。

```app.vue
<template>
  <div>
    <NuxtPage />
  </div>
</template>
```

pages/index.vue に実装。

```pages/index.vue
<script setup>
// vue-datepicker
import VueDatePicker from '@vuepic/vue-datepicker'
// style
import '@vuepic/vue-datepicker/dist/main.css'

// modelValue
const date = ref(new Date())

</script>

<template>
  <div>
    <div>
      <h1>index.vue</h1>
    </div>

    <div>
      <VueDatePicker v-model="date" locale="ja" format="yyyy/MM/dd HH:mm:ss" enable-seconds />
    </div>
    <div>
      {{ date }}<br />
      {{ typeof date }}<br />
      {{ date instanceof Date }}
    </div>
  </div>
</template>

<style lang="css"></style>

```



