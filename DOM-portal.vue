<script setup>
// Vue.js provides a built-in component
// that renders its slot content to another part of the DOM.

import {Teleport} from "vue"
const msg = "Hello World"

</script>

<template>
  <!-- Renders it to a child element of the `body` -->
  <Teleport to="body">
      <span>{{ msg }}</span>
    </Teleport>
</template>