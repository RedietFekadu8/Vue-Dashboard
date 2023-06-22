<template>
    <div class="charts">
  <div id="chart">
        <apexchart type="donut" :options="chartOptions" :series="series"></apexchart>
      </div>
     </div> 
</template>

<script>
export default {
    data(){
          return {          
          series: [44, 55, 41, 17, 15],
          chartOptions: {
            chart: {
              type: 'donut',
            },
            responsive: [{
              breakpoint: 480,
              options: {
                aspectRatio: 1,
                chart: {
                  width: 200
                },
                legend: {
                  position: 'bottom'
                }
              }
            }]
          },
          
        }
        }
        
    }
    

</script>

<style>
 
</style>