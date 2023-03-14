<template>
  <h2>origin table</h2>
  <div
    class="el-table--mini el-table"
    data-prefix="el" data-v-7a7a37b1="" style="width: 100%;">
    <div class="el-table__inner-wrapper">
      <div class="el-table__header-wrapper">
        <table class="el-table__header" border="0" cellpadding="0" cellspacing="0" style="width: 100%">
          <thead class="">
            <tr class="">
              <th class="el-table_1_column_1 is-leaf el-table__cell" colspan="1" rowspan="1">
                <div class="cell">Date</div>
              </th>
              <th class="el-table_1_column_2 is-leaf el-table__cell" colspan="1" rowspan="1">
                <div class="cell">Name</div>
              </th>
              <th class="el-table_1_column_3 is-leaf el-table__cell" colspan="1" rowspan="1">
                <div class="cell">Address</div>
              </th>
            </tr>
          </thead>
        </table>
      </div>
      <div class="el-table__body-wrapper">
        <div class="el-scrollbar">
          <div class="el-scrollbar__wrap el-scrollbar__wrap--hidden-default">
            <div class="el-scrollbar__view" style="display: inline-block; vertical-align: middle;">
              <table class="el-table__body" cellspacing="0" cellpadding="0" border="0"
                style="table-layout: fixed; width: 100%;">
                <tbody>
                  <tr class="el-table__row" v-for="item in data">
                    <td class="el-table_1_column_1 el-table__cell" rowspan="1" colspan="1">
                      <div class="cell">{{ item.date }}</div>
                    </td>
                    <td class="el-table_1_column_2 el-table__cell" rowspan="1" colspan="1">
                      <div class="cell">{{ item.name }}</div>
                    </td>
                    <td class="el-table_1_column_3 el-table__cell" rowspan="1" colspan="1">
                      <div class="cell">{{ item.address }}</div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps({
  num: {
    type: Number,
    default: 1000,
  },
})
const data = computed(() => {
  return Array.from({ length: props.num }).fill('').map((_, index) => ({
    id: index,
    date: '2016-05-03',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles No.',
  }))
})
</script>