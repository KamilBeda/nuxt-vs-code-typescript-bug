<script setup lang="ts">
function doSomething() {
  console.log("hello");
}

const images = ref([]);
</script>

<template>
  <WithSlots>
    Hello
    <template v-if="images.length === 0" #subtitle>
      <span>World</span>
    </template>
    <template v-else-if="images.length === 1" #caption>
      <span @click="doSomething">Caption</span>
    </template>
    <template v-else #caption>
      <span @click="doSomething">Caption</span>
    </template>
  </WithSlots>
</template>
