<script setup>
import { storeToRefs } from 'pinia';
import Chart from './Chart.vue';
import Chart2 from './Chart2.vue';  
import Chart3 from './Chart3.vue';

import { useAuthStore } from '@/stores';

const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
    
    <div id="chart">
        <Chart />
    </div>

    <div id="chart2">
        <Chart2 />
    </div>
    <div id="chart3"> 
        <Chart3 />
        </div>
    
</template>
<style>
  .charts{
    display:flex; 
    align-items: center;
    justify-content: center;
  }
  .chart{
    width: 250px;
    padding: 20px;
    border-radius: 20px;
  }

</style>