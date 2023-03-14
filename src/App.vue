<script setup lang="ts">
import { markRaw, ref } from 'vue'
import Home from './components/Home.vue'
import ElTableDemo from './components/ElTableDemo.vue'
import OriginTableDemo from './components/OriginTableDemo.vue'
const currentPage = ref<any>(markRaw(Home))
</script>

<template>
  <div class="layout">
    <div class="header">
      <div class="link" @click="currentPage = markRaw(Home)">Home</div>
      <div class="link" @click="currentPage = markRaw(ElTableDemo)">ElTableDemo</div>
      <div class="link" @click="currentPage = markRaw(OriginTableDemo)">OriginTableDemo</div>
    </div>
    <div class="content">
      <component :is="currentPage" />
    </div>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  gap: 20px;
}

.link {
  cursor: pointer;
}
</style>


