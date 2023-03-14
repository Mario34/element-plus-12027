<template>
  <h2>ElTable</h2>
  <el-table :data="data" style="width: 100%">
    <el-table-column prop="date" label="Date" />
    <el-table-column prop="name" label="Name" />
    <el-table-column prop="address1" label="Address" show-overflow-tooltip />
  </el-table>
</template>

<script setup lang="ts">
const props = defineProps({
  num: {
    type: Number,
    default: 1000,
  },
})
const data = Array.from({ length: props.num }).fill('').map((_, index) => ({
  id: index,
  date: '2016-05-03',
  name: 'Tom',
  address1: 'No. 189, Grove St, Los Angeles No.',
}))
</script>