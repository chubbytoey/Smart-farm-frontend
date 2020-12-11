<script>
import { Line } from 'vue-chartjs'
export default {
  extends: Line,
  props: {
    data: {
      type: Object,
      default: null
    }
  },
  watch: {
    data (value) {
      this.renderChart(value)
    }
  }
}
</script>
