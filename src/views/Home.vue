<script setup>
import { storeToRefs } from 'pinia';
// import Chart from './Chart.vue';
// import Chart2 from './Chart2.vue';
import ChartAll from './ChartAll.vue';

import { useAuthStore } from '@/stores';


const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
    <div v-if="user">
        <h1>Hi {{user.firstName}} {{ user.lastName }}</h1>
        <h2>Welcome to the Dashboard</h2>
      
        <!-- <p><router-link to="/users">Manage Users</router-link></p> -->
    <!-- </div>
    <div id="chart">
        <Chart />
    </div>

    <div id="chart2">
        <Chart2 />
    </div>
     -->
     <!-- <ChartAll /> -->
    </div>
</template>
<style>
#chart{
    width: 500px;
}
#chart2{
    display: flex;
    left: 50px;
    width: 20px;
}

</style>