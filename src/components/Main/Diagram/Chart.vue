<template>
  <div class="round">
    <img :src="logo" alt="logo" class="round__logo"/>
    <apexchart type="donut" :options="chartOptions" :series="chartData.employeesNumbers" />
  </div>
</template>

<script>
import VueApexCharts from "vue-apexcharts"
import logo from "@/assets/logoNeurosoft.png"

export default {
  components: {
    apexchart: VueApexCharts
  },
  props: {
    chartData: Object
  },
  data() {
    return {
      logo, 
      chartOptions: {
        labels: this.chartData.titles,
        chart: {
          type: 'donut',
        },
        legend: {
          position: 'right',
          horizontalAlign: 'center', 
          floating: false,
          fontSize: '22px',
          fontFamily: 'roboto',
          fontWeight: 500,
          height: 590,
          offsetX: -100,
          offsetY: 0,
          labels: {
            colors: undefined,
            useSeriesColors: false
          },
          markers: {
            width: 35,
            height: 35,
            radius: 50,
            offsetX: 0,
            offsetY: 0
          },
          itemMargin: {
            horizontal: 0,
            vertical: 11
          }
        },
        colors: ["#2B78FE", "#8295FA", "#FFBB49", "#87D227", "#20CBAC", "#01B0D7", "#6235B0", "#9559FF", "#C055D1", "#FF7979"],
        responsive: [{
          breakpoint: 1201,
          options: {
            legend: {
              fontSize: '18px',
              height: 475,
              offsetX: -75,
              offsetY: 0,
              markers: {
                width: 25,
                height: 25,
                radius: 50,
                offsetX: 0,
                offsetY: 0
              },
              itemMargin: {
                horizontal: 0,
                vertical: 11
              },
            }
          }
        }]
      },
    }
  }
}
</script>

<style lang="scss">
  /* Не получилось отцентрировать элементы списка с помощью настроек в apexchartjs
  поэтому использовал данные "костыли" */
  .apexcharts-legend-series {
    display: flex;
    align-items: center;
  }
  
  .apexcharts-legend-text {
    margin-left: 23px;
  }

  /* Также не придумал как лучше реализовать серую "обводку" у списка 
  поэтому оставил просто бордер*/
  .apexcharts-legend {
    border-left: 3px solid #C1C3C8;
  }

  .round {
    position: relative;
    margin-top: 72px;
  }

  .round__logo {
    position: absolute;
    top: 236px;
    left: 258px;
  }
</style>