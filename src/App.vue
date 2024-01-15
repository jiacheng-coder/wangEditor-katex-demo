<template>
  <div>
    wangEditor for vue3
    <button @click="toggle">显示/隐藏</button>
  </div>
  <hr>

  <BasicEditor v-show="show"></BasicEditor>
  <!-- <ExtendedEditor v-if="show"></ExtendedEditor> -->
</template>

<script setup>
import { ref } from 'vue'
import BasicEditor from './components/BasicEditor.vue'
import ExtendedEditor from './components/ExtendedEditor.vue'

const show = ref(true)
function toggle() {
  show.value = !show.value
}
</script>
