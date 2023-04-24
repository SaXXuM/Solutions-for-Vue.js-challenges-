<script setup>
// Please validate the type prop of the Button component.
// It's accept the following strings
// primary | ghost | dashed | link | text | default only
// and the default value is default.

defineProps({
  type: {
  	type: String,
  	validator: (value) => ['primary', 'ghost', 'dashed', 'link', 'text', 'default'].includes(value),
  	default: 'default'
  }
})
</script>

<template>
  <button>Button</button>
</template>