<script>
import { Line } from 'vue-chartjs'
export default {
  extends: Line,
  mounted () {
    this.renderChart(
      {
        labels: [
          'day 2',
          'day 3',
          'day 4',
          'day 5',
          'day 6',
          'day 7',
          'day 8'
        ],
        datasets: [
          {
            label: 'max',
            data: [2, 10, 5, 9, 0, 6, 20],
            backgroundColor: 'transparent',
            borderColor: 'rgba(255, 0,0, 0.35)',
            pointBackgroundColor: 'rgba(255, 0, 0)'
          },
          {
            label: 'min',
            data: [10, 20, 30, 39, 10, 3, 39],
            backgroundColor: 'transparent',
            borderColor: 'rgba(0, 231, 255, 0.35)',
            pointBackgroundColor: 'rgba(0, 231, 255)'
          },
          {
            label: 'min',
            data: [30, 2, 13, 8, 3, 48, 20],
            backgroundColor: 'transparent',
            borderColor: 'rgba(300, 220, 124,0.35)',
            pointBackgroundColor: 'rgba(300, 220, 124)'
          }
        ]
      },
      {
        responsive: true,
        maintainAspectRatio: true,
        title: {
          display: true,
          text: 'temperature for 7 days'
        }
      }
    )
  }
}
</script>
