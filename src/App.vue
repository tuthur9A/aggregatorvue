<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="jobs-list">
    <h1 class="title">Aggregateur de Jobs</h1>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </div>
</template>

<style scoped>
.jobs-list {
  display: flex;
  flex-flow: column;
  justify-content: flex-start;
}
.title {
  text-align: center;
  font-size: 1.5em;
}
.wrapper {
  display: flex;
  flex-flow: row;
  justify-content: center;
  align-items: center;
}
</style>
