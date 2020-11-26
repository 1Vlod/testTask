<template>
  <div class="info">
    <InfoCard 
      v-for="(value, name) in infoData" 
      :key="name"
      :number="Number(value)"
      :name="name"
    />
  </div>
</template>

<script>
import InfoCard from "./InfoCard"
import testData from "@/assets/test.json"

export default {
  name: "Info",
  components: {
    InfoCard
  },
  data: () => {
    return {
      infoData: {
        "Сотрудников в штате": testData.data.total,
        "Мужчины": testData.data.males,
        "Женщины": testData.data.females,
        "Пар": testData.data.couples,
      }
    }
  }  
}
</script>

<style scoped lang="scss">
  .info {
    max-width: 940px;

    display: flex;
    justify-content: space-between;
  }
</style>