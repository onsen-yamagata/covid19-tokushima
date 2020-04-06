<script lang="ts">
import Vue from 'Vue'
export default Vue.extend({
  fetch({ redirect }) {
    redirect(301, 'https://stopcovid19-yamagata.netlify.com/')
  }
})
</script>
