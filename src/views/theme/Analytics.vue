<template>
  <div class="bg">
    <CRow>
      <CCol>
        <WidgetsStatsA />
      </CCol>
    </CRow>
  </div>
</template>

<script>
import WidgetsStatsA from '../widgets/WidgetsStatsTypeA.vue'

export default {
  name: 'Analytics',
  components: {
    WidgetsStatsA,
  },
}
</script>
