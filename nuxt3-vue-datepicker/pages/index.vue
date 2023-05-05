<script setup>
// vue-datepicker
import VueDatePicker from '@vuepic/vue-datepicker'
// style
import '@vuepic/vue-datepicker/dist/main.css'

// modelValue
const date = ref('2023/05/05 05:55:00')

</script>

<template>
  <div>
    <div>
      <h1>index.vue</h1>
    </div>

    <div>
      <VueDatePicker v-model="date" model-type="yyyy/MM/dd HH:mm:ss" locale="ja" format="yyyy/MM/dd HH:mm:ss"
        enable-seconds />
    </div>
    <div>
      {{ date }}<br />
      {{ typeof date }}<br />
      {{ date instanceof Date }}
    </div>
  </div>
</template>

<style lang="css"></style>
