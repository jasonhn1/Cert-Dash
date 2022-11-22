<template>
  <CRow>
    <CCol>
      <WidgetsStatsA />
    </CCol>
  </CRow>
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
