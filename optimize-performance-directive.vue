<script setup>
// Vue.js provides a directive that renders the element
// and the component only once, and skips future updates.

import { ref } from "vue"

const count = ref(0)

setInterval(() => {
  count.value++
}, 1000)
</script>

<template>
  <span v-once>Make it never change: {{ count }}</span>
</template>