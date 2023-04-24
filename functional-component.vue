<script setup lang='ts'>
/**
 * Implement a functional component :
 * 1. Render the list elements (ul/li) with the list data
 * 2. Change the list item text color to red when clicked.
*/

import { ref, h } from "vue"

const ListComponent = (props, { emit }) => {
  return h('ul', props.list.map((item, index) => h('li', {
    style: {color: props['active-index'] === index ? 'red' : 'inherit' },
    onClick: () => { emit('toggle', index) }
  }, item.name)))
}

const list = [{
  name: "John",
}, {
  name: "Doe",
}, {
  name: "Smith",
}]

const activeIndex = ref(0)

function toggle(index: number) {
  activeIndex.value = index
}

</script>

<template>
  <list-component
    :list="list"
    :active-index="activeIndex"
    @toggle="toggle"
  />
</template>
