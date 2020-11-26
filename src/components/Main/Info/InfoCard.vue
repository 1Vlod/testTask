<template>
  <div class="card">
    <div class="card__number">{{ number }}</div>
    <div class="card__name">{{ name }}</div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    number: Number
  }
}
</script>

<style lang="scss" scoped>
  .card {
    max-width: 166px;
  }
  
  .card__number {
    font-style: normal;
    font-weight: 900;
    font-size: 80px;

    line-height: 94px;
    text-align: center;

    color: #2B78FE;
  }

  .card__name {
    font-style: normal;
    font-weight: normal;
    font-size: 24px;

    line-height: 30px;
    text-align: center;

    color: #353D54;
  }
</style>