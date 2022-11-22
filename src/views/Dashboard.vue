<template>
  <div>
    <CRow>
      <CCol :md="12">
        <CCard class="mb-4">
          <CCardHeader class="card-bg"> <h2>Candidate Links</h2> </CCardHeader>
          <CCardBody class="card-bg">
            <CTable
              align="middle"
              class="mb-0 border table-bg"
              hover
              responsive
            >
              <CTableHead color="light">
                <CTableRow>
                  <CTableHeaderCell>Name</CTableHeaderCell>
                  <CTableHeaderCell>Status</CTableHeaderCell>
                  <CTableHeaderCell class="text-center"
                    >Country</CTableHeaderCell
                  >
                  <CTableHeaderCell class="text-center">Date</CTableHeaderCell>
                  <CTableHeaderCell></CTableHeaderCell>
                </CTableRow>
              </CTableHead>
              <CTableBody>
                <CTableRow v-for="item in tableExample" :key="item.name">
                  <CTableDataCell>
                    <div>{{ item.user.name }}</div>
                  </CTableDataCell>
                  <CTableDataCell>
                    <CButton
                      :color="item.status.color"
                      class="btn-sm rounded-pill text-btn"
                    >
                      {{ item.status.text }}
                    </CButton>
                  </CTableDataCell>
                  <CTableDataCell class="text-center">
                    <CIcon
                      size="xl"
                      :name="item.country.flag"
                      :title="item.country.name"
                    />
                  </CTableDataCell>
                  <CTableDataCell class="text-center">
                    <div>{{ item.date }}</div>
                  </CTableDataCell>
                  <CTableDataCell>
                    <button type="button" class="btn btn-outline-info">
                      View
                    </button>
                  </CTableDataCell>
                </CTableRow>
                <CTableRow> </CTableRow>
              </CTableBody>
            </CTable>
          </CCardBody>
        </CCard>
      </CCol>
    </CRow>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  setup() {
    const tableExample = [
      {
        user: {
          name: 'Jeffery Dharma',
        },
        country: { name: 'USA', flag: 'cif-us' },
        status: {
          color: 'success',
          text: 'Ready',
        },
        usage: {
          value: 50,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'success',
        },
        date: '12/31/2022',
        activity: '10 sec ago',
      },
      {
        user: {
          name: 'Tim Cooks',
        },
        status: {
          color: 'success',
          text: 'Ready',
        },
        country: { name: 'USA', flag: 'cif-us' },
        usage: {
          value: 50,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'success',
        },
        date: '9/12/2022',
        activity: '10 sec ago',
      },
      {
        user: {
          name: 'Ben Ten',
        },
        status: {
          color: 'success',
          text: 'Ready',
        },
        country: { name: 'USA', flag: 'cif-us' },
        usage: {
          value: 50,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'success',
        },
        date: '6/12/2022',
        activity: '10 sec ago',
      },
      {
        user: {
          name: 'Jason Duerlo',
        },
        status: {
          color: 'warning',
          text: 'Waiting',
        },
        country: { name: 'USA', flag: 'cif-us' },
        usage: {
          value: 50,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'success',
        },
        date: '1/1/2022',
        activity: '10 sec ago',
      },
      {
        user: {
          name: 'Donny Trump',
        },
        status: {
          color: 'warning',
          text: 'Waiting',
        },
        country: { name: 'Spain', flag: 'cif-es' },
        usage: {
          value: 22,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'primary',
        },
        date: '12/14/2022',
        activity: 'Last week',
      },
      {
        user: {
          name: 'Brock Obama',
        },
        status: {
          color: 'danger',
          text: 'Expired',
        },
        country: { name: 'Poland', flag: 'cif-pl' },
        usage: {
          value: 43,
          period: 'Jun 11, 2021 - Jul 10, 2021',
          color: 'success',
        },
        date: '3/5/2021',
        activity: 'Last week',
      },
    ]

    return {
      tableExample,
    }
  },
}
</script>
