<template>
  <div class="container">
    <div class="chartContainer">
      <label v-if="userId">{{ userId }}</label>
      <LineChart :data="tempDataOneWeek" class="chart" :width="300" />
    </div>
    <div class="copyContainer">
      <input id="copyText" type="text" value="https://liff.line.me/1655371433-VdNEZGNE">
      <button @click="copyLink">
        Copy
      </button>
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
      userId: null,
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 2,
                          max: 100,
                          avg: 30
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 1000,
                          max: 23,
                          avg: 90
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 34,
                          max: 131,
                          avg: 3412
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 120,
                          avg: 300
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 10,
                          max: 230,
                          avg: 300
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 40,
                          max: 310,
                          avg: 3222
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
                    },
                    {
                      device_id: 'toey',
                      temperature: [
                        {
                          device_id: 1,
                          min: 23,
                          max: 510,
                          avg: 1320
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
                }
              }
            }
          }
        },
      tempDataOneWeek: null,
      farmUser: null
    }
  },
  watch: {
    // userId () {
    //   this.fetchData()
    // },
    farmUser () {
      this.fillData()
    }
  },
  async beforeMount () {
    await liff.init({ liffId: '1655371433-VdNEZGNE' })
  },
  async mounted () {
    if (!liff.isLoggedIn() && liff.getOS() === 'web') { return liff.login() }

    const profile = await liff.getProfile()
    this.userId = profile.userId
    this.fetchData(this.userId)
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
          },
          {
            label: 'min',
            data: this.fillDatasets('min'),
            backgroundColor: 'transparent',
            borderColor: 'rgba(255, 200,0, 0.35)',
            pointBackgroundColor: 'rgba(255, 200, 0)'
          },
          {
            label: 'avg',
            data: this.fillDatasets('avg'),
            backgroundColor: 'transparent',
            borderColor: 'rgba(96, 168,48, 0.35)',
            pointBackgroundColor: 'rgba(96, 168,48)'
          }
        ]
      }
    },
    fillDatasets (input) {
      const dataMock = []
      const apiData = this.tempRawOneWeek.data.dataInOneWeek.data
      Object.values(apiData).forEach((value, key) => {
        if (input === 'max') {
          dataMock.push(value.device[this.farmUser].temperature[0].max)
        } else if (input === 'min') {
          dataMock.push(value.device[this.farmUser].temperature[0].min)
        } else {
          dataMock.push(value.device[this.farmUser].temperature[0].avg)
        }
      })
      return dataMock
    },
    copyLink () {
      const link = document.querySelector('#copyText')
      link.select()
      document.execCommand('copy')
    },
    fetchData (userID) {
      fetch(`https://mysterious-journey-03229.herokuapp.com/getfarm?user_id=${userID}`)
        .then(res => res.json()).then((res) => {
          console.log('on', userID)
          this.farmUser = res.farm_id - 1
        })
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
  justify-content: center;
  flex-direction: column;
}
@media screen and (max-width: 414px) {
  .container {
    width: 100vw;
    & > .copyContainer{
      margin-top: 20px;
      & > input {
        border: 1px solid rgba(0,0,0,0.25);
        border-radius: 4px;
        padding: 2px 5px;
      }
      & > button {
        background-color: #4EA72EFF;
        border: none;
        color: #fff;
        border-radius: 4px;
        width: 54px;
      }
    }
    & > .chartContainer {
      margin:0 auto;
    }

  }
}
</style>
