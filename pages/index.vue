<template>
  <div class="container">
    <div class="chartContainer">
      {{ userId }}
      <label>plz</label>
      <LineChart :data="tempDataOneWeek" class="chart" width="330px" height="300px" />
    </div>
  </div>
</template>

<script>
import liff from '@line/liff'
import LineChart from '../components/LineChart'

export default {
  components: {
    LineChart
  },
  data () {
    return {
      userId: '',
      tempRawOneWeek:
        {
          status: 200,
          data: {
            dataInOneWeek: {
              data: {
                dataOn1stDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 56,
                          max: 99,
                          avg: 87
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 59,
                          max: 78,
                          avg: 79
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 13,
                          max: 51,
                          avg: 79
                        }
                      ],
                      pm_10: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 120
                        }
                      ],
                      pm_25: [
                        {
                          device_id: 1,
                          min: 4,
                          max: 50,
                          avg: 25
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 12,
                          max: 22,
                          avg: 32
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 10,
                          max: 100,
                          avg: 50
                        }
                      ]
                    }
                  ]
                },
                dataOn2ndDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 20,
                          max: 200,
                          avg: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                },
                dataOn3rdDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 10,
                          max: 22,
                          avg: 20
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                },
                dataOn4thDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 84,
                          max: 392,
                          avg: 20
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                },
                dataOn5thDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 2,
                          max: 340,
                          avg: 31
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                },
                dataOn6thDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 24,
                          max: 470,
                          avg: 99
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                },
                dataOn7thDay: {
                  device: [
                    {
                      device_id: 'jzo',
                      temperature: [
                        {
                          device_id: 1,
                          min: 10,
                          max: 842,
                          avg: 249
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min: 30,
                          max: 300,
                          avg: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 400,
                          avg: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min: 50,
                          max: 500,
                          avg: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min: 60,
                          max: 600,
                          avg: 90
                        }
                      ]
                    }
                  ]
                }
              }
            }
          }
        },
      tempDataOneWeek: null
    }
  },
  mounted () {
    liff.init({ liffId: '1655371433-VdNEZGNE' }, () => {
      if (liff.isLoggedIn()) {
        liff.getProfile().then((profile) => {
          console.log(profile.userId)
          const userId = profile.userId
          this.userId = userId
        }).catch(err => console.log(err))
      } else {
        liff.login()
      }
    }, err => console.error(err.code, err.message))
    this.fillData()
  },
  methods: {
    fillData () {
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
            data: this.fillDatasets('max'),
            backgroundColor: 'transparent',
            borderColor: 'rgba(255, 0,0, 0.35)',
            pointBackgroundColor: 'rgba(255, 0, 0)'
          }
        ]
      }
    },
    fillDatasets (input) {
      const dataMock = []
      const apiData = this.tempRawOneWeek.data.dataInOneWeek.data
      Object.values(apiData).forEach((value, key) => {
        dataMock.push(value.device[0].temperature[0].input)
      })
      console.log(input, ' : ', dataMock)
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
