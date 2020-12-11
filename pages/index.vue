<template>
  <div class="container">
    <div class="chartContainer">
      <LineChart :data="tempDataOneWeek" class="chart" width="330px" height="300px" />
    </div>
  </div>
</template>

<script>
import LineChart from '../components/LineChart'
export default {
  components: {
    LineChart
  },
  data () {
    return {
      tempRawOneWeek: [
        {
          status: 200,
          data: [
            {
              id_device: '1',
              type: 'temp',
              value: {
                avg: 12,
                max: 23,
                min: 21
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'humidity',
              value: {
                avg: 30,
                max: 120,
                min: 31
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_1',
              value: {
                avg: 30,
                max: 24,
                min: 12
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_10',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_25',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'wind_velocity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pressure',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },

            {
              id_device: '1',
              type: 'temp',
              value: {
                avg: 50,
                max: 22,
                min: 25
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'humidity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_1',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_10',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pm_25',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'wind_velocity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '1',
              type: 'pressure',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'temp',
              value: {
                avg: 94,
                max: 48,
                min: 94
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'humidity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_1',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_10',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_25',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'wind_velocity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pressure',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-12-05T13:42:00Z'
            },

            {
              id_device: '2',
              type: 'temp',
              value: {
                avg: 23,
                max: 62,
                min: 41
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'humidity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_1',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_10',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pm_25',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'wind_velocity',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            },
            {
              id_device: '2',
              type: 'pressure',
              value: {
                avg: 20,
                max: 20,
                min: 20
              },
              timestamp: '2020-11-05T13:42:00Z'
            }
          ]
        }
      ],
      tempDataOneWeek: null
    }
  },
  mounted () {
    this.fillData()
  },
  methods: {
    fillData () {
      console.log('yahoo')
      this.tempDataOneWeek = {
        labels: [
          'day 1',
          'day 2',
          'day 3',
          'day 4',
          'day 5',
          'yest',
          'today'
        ],
        datasets: [
          {
            label: 'max',
            data: this.fillDatasets(),
            backgroundColor: 'transparent',
            borderColor: 'rgba(255, 0,0, 0.35)',
            pointBackgroundColor: 'rgba(255, 0, 0)'
          }
        ]
      }
    },
    fillDatasets () {
      const dataMock = []
      for (let j = 0; j < this.tempRawOneWeek[0].data.length; j++) {
        if (this.tempRawOneWeek[0].data[j].id_device === '1') {
          if (this.tempRawOneWeek[0].data[j].type === 'temp') {
            dataMock.push(this.tempRawOneWeek[0].data[j].value.avg)
          }
        }
      }
      console.log(dataMock)
      return dataMock
    }
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
    & > .chartContainer {
      margin:0 auto;
    }

  }
}
</style>
