<template>
  <div class="container">
    <div>
      <h1 class="title">
        Smart FARM
      </h1>
      <LineChart />
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

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
@media screen and (max-width: 414px) {
  .title{
    color:red;
  }
  .imgBG {
    width: 100%;
  }
}
</style>
