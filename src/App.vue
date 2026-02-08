<template>
  <div ref="el">
    <div v-for="item in list" :key="item.id" class="item">
      <span>{{ item.name }}</span>
    </div>
  </div>
</template>
<script setup lang="ts">
import { shallowRef, useTemplateRef } from 'vue'
import { useSortable } from '@vueuse/integrations/useSortable'

const el = useTemplateRef('el')
const list = shallowRef([{ id: 1, name: 'a' }, { id: 2, name: 'b' }, { id: 3, name: 'c' }])

useSortable(el, list, {
  animation: 150 // Throws: Object literal may only specify known properties, and 'animation' does not exist in type 'UseSortableOptions'.
})
</script>
<style>
.item {
  background: gray;
  margin: 5px;
  padding: 5px;
}
</style>
