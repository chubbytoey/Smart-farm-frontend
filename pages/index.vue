<template>
  <div class="container">
    <div class="chartContainer">
      {{ userId }}
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
                          min_humudity: 56,
                          max_humudity: 99,
                          avg_humudity: 87
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 59,
                          max_humudity: 78,
                          avg_humudity: 79
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 13,
                          max_pm_1: 51,
                          avg_pm_1: 79
                        }
                      ],
                      pm_10: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 120
                        }
                      ],
                      pm_25: [
                        {
                          device_id: 1,
                          min_pm_1: 4,
                          max_pm_1: 50,
                          avg_pm_1: 25
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 12,
                          max_wind_velocity: 22,
                          avg_wind_velocity: 32
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 10,
                          max_pressure: 100,
                          avg_pressure: 50
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
                          min_humudity: 20,
                          max_humudity: 200,
                          avg_humudity: 50
                        }
                      ],
                      humidity: [
                        {
                          device_id: 1,
                          min_humudity: 30,
                          max_humudity: 300,
                          avg_humudity: 60
                        }
                      ],
                      pm_1: [
                        {
                          device_id: 1,
                          min_pm_1: 40,
                          max_pm_1: 400,
                          avg_pm_1: 70
                        }
                      ],
                      wind_velocity: [
                        {
                          device_id: 1,
                          min_wind_velocity: 50,
                          max_wind_velocity: 500,
                          avg_wind_velocity: 80
                        }
                      ],
                      pressure: [
                        {
                          device_id: 1,
                          min_pressure: 60,
                          max_pressure: 600,
                          avg_pressure: 90
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
      // for (let j = 0; j < this.tempRawOneWeek[0].data.dataInOneWeek.data; j++) {
      //   if (this.tempRawOneWeek[0].data[j].id_device === '1') {
      //     if (this.tempRawOneWeek[0].data[j].type === 'temp') {
      //       dataMock.push(this.tempRawOneWeek[0].data[j].value.avg)
      //     }
      //   }
      // }
      // console.log(Object.values(this.tempRawOneWeek.data.dataInOneWeek.data))
      const apiData = this.tempRawOneWeek.data.dataInOneWeek.data
      // const finshResult = Object.values(apiData).forEach((value,key) => {

      // })
      console.log('test', Object.values(apiData).forEach((value, key) => {
        console.log(value.device[0].temperature[0].max_humudity, '++++', key)
      }))
      console.log('hey' + this.userId)
      // for (const [key, value] of Object.entries(apiData)) {
      //   console.log(`${key}: ${value}`)
      // }
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
