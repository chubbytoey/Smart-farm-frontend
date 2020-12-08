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
            label: 'temperature',
            data: [2, 10, 5, 9, 0, 6, 20],
            backgroundColor: 'transparent',
            borderColor: 'rgba(1, 116, 188, 0.50)',
            pointBackgroundColor: 'rgba(171, 71, 188, 1)'
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
