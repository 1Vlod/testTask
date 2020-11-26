<template>
  <div class="diagram">
    <div class="diagram__title">
      По департаментам
    </div>
    <Chart :chartData="{titles, employeesNumbers}"/>
  </div>
</template>

<script>
import Chart from "./Chart"
import test from "@/assets/test.json"

export default {
  components: {
    Chart
  },

  data() {
    return {
      titles: [],
      employeesNumbers: []
    }
  },

  created() {
    this.titles = test.data.departments.reduce( (acc, item) => {
      acc.push(item.title)
      return acc
    }, [])
    
    this.employeesNumbers = test.data.departments.reduce( (acc, item) => {
      acc.push(item.employees)
      return acc
    }, [])
  }
}
</script>

<style lang="scss" scoped>
  .diagram {
    margin-top: 100px;
  }

  .diagram__title {
    font-weight: 500;
    font-size: 30px;
    line-height: 22px;

    color: #353D54;
  }
</style>