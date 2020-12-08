<template>
  <div class="container">
    <div>
      <LineChart class="chart"/>
    </div>
  </div>
</template>

<script>
import LineChart from '../components/LineChart'
export default {
  components: {
    LineChart
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  align-items: center;
  text-align: center;
}
@media screen and (max-width: 414px) {
  .container {
    width: 100vw;
    & > .chart {
      margin: 0 20px;
    }
  }
}
</style>
