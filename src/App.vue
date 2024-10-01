<template>
  <table>
    <thead>
      <tr>
        <th colspan="2"></th>
        <th colspan="4" v-for="month in months" :key="month">{{ month }}</th>
      </tr>
      <tr>
        <th>Status</th>
        <th>Datetime</th>
        <th v-for="(day, index) in days" :key="index">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month2' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month3' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month4' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month5' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month6' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month7' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month8' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month9' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month10' + index + day">{{ day }}</th>
        <th v-for="(day, index) in days" :key="'month11' + index + day">{{ day }}</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Pending</td>
        <td>2024-07-01</td>
        <td v-for="tableData in tableDatas" :key="tableData" :style="{ backgroundColor: tableData === 'True' ? 'blue' : 'grey'}">{{ tableData }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script setup>
import { ref } from 'vue';

const days = [1, 2, 3, 4];

const months = [
  'เดือน 1', 'เดือน 2', 'เดือน 3', 'เดือน 4',
  'เดือน 5', 'เดือน 6', 'เดือน 7', 'เดือน 8',
  'เดือน 9', 'เดือน 10', 'เดือน 11', 'เดือน 12'
];

const tableDatas = ref([
  'False', 'False', 'True', 'False', 'False', 'True', 'False', 'False', 'False', 'False', 'False', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True', 'False', 'True', 'True', 'True',
]);
</script>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  border: 1px solid #000;
  padding: 8px;
  text-align: center;
}
</style>
