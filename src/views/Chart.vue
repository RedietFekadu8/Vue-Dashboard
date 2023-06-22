<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="charts">
      <div id="chart" >
          <apexchart type="bar" height="450" width="825" :options="chartOptions" :series="series"></apexchart>
      </div>
      
    </div>
  </template>
  
  <script>
  export default {
      data(){
          return{
              series: [{
              name: 'Net Profit',
              data: [44, 55, 57, 56, 61, 58, 63, 60, 66]
            }, {
              name: 'Revenue',
              data: [76, 85, 101, 98, 87, 105, 91, 114, 94]
            }, {
              name: 'Free Cash Flow',
              data: [35, 41, 36, 26, 45, 48, 52, 53, 41]
            }],
            chartOptions: {
              chart: {
                type: 'bar',
                height: 350
              },
              plotOptions: {
                bar: {
                  horizontal: false,
                  columnWidth: '55%',
                  endingShape: 'rounded'
                },
              },
              dataLabels: {
                enabled: false
              },
              stroke: {
                show: true,
                width: 2,
                colors: ['transparent']
              },
              xaxis: {
                categories: ['Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct'],
              },
              yaxis: {
                title: {
                  text: '$ (thousands)'
                }
              },
              fill: {
                opacity: 1
              },
              tooltip: {
                y: {
                  formatter: function (val) {
                    return "$ " + val + " thousands"
                  }
                }
              }
            },
            //2nd
            series2: [44, 55, 13, 43, 22],
            chartOptions2: {
              chart: {
                width: 380,
                type: 'pie',
              },
              labels: ['Team A', 'Team B', 'Team C', 'Team D', 'Team E'],
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
            //3rd
            series3: [{
              data: [400, 430, 448, 470, 540, 580, 690, 1100, 1200, 1380]
            }],
            chartOptions3: {
              chart: {
                type: 'bar',
                height: 380
              },
              plotOptions: {
                bar: {
                  barHeight: '100%',
                  distributed: true,
                  horizontal: true,
                  dataLabels: {
                    position: 'bottom'
                  },
                }
              },
              colors: ['#33b2df', '#546E7A', '#d4526e', '#13d8aa', '#A5978B', '#2b908f', '#f9a3a4', '#90ee7e',
                '#f48024', '#69d2e7'
              ],
              dataLabels: {
                enabled: true,
                textAnchor: 'start',
                style: {
                  colors: ['#fff']
                },
                formatter: function (val, opt) {
                  return opt.w.globals.labels[opt.dataPointIndex] + ":  " + val
                },
                offsetX: 0,
                dropShadow: {
                  enabled: true
                }
              },
              stroke: {
                width: 1,
                colors: ['#fff']
              },
              xaxis: {
                categories: ['South Korea', 'Canada', 'United Kingdom', 'Netherlands', 'Italy', 'France', 'Japan',
                  'United States', 'China', 'India'
                ],
              },
              yaxis: {
                labels: {
                  show: false
                }
              },
              title: {
                  text: 'Custom DataLabels',
                  align: 'center',
                  floating: true
              },
              subtitle: {
                  text: 'Category Names as DataLabels inside bars',
                  align: 'center',
              },
              tooltip: {
                theme: 'dark',
                x: {
                  show: false
                },
                y: {
                  title: {
                    formatter: function () {
                      return ''
                    }
                  }
                }
              }
            },
            //4th
            series4: [{
              name: 'Website Blog',
              type: 'column',
              data: [440, 505, 414, 671, 227, 413, 201, 352, 752, 320, 257, 160]
            }, {
              name: 'Social Media',
              type: 'line',
              data: [23, 42, 35, 27, 43, 22, 17, 31, 22, 22, 12, 16]
            }],
            chartOptions4: {
              chart: {
                height: 350,
                type: 'line',
              },
              stroke: {
                width: [0, 4]
              },
              title: {
                text: 'Traffic Sources'
              },
              dataLabels: {
                enabled: true,
                enabledOnSeries: [1]
              },
              labels: ['01 Jan 2001', '02 Jan 2001', '03 Jan 2001', '04 Jan 2001', '05 Jan 2001', '06 Jan 2001', '07 Jan 2001', '08 Jan 2001', '09 Jan 2001', '10 Jan 2001', '11 Jan 2001', '12 Jan 2001'],
              xaxis: {
                type: 'datetime'
              },
              yaxis: [{
                title: {
                  text: 'Website Blog',
                },
              
              }, {
                opposite: true,
                title: {
                  text: 'Social Media'
                }
              }]
            },
           
    }}
  
  }
  </script>
  
  <style>


  </style>