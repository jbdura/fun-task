<script setup>
const plans = [
  {
    title: "Subscription Plan",
    details: {
      function: true,
      responsive: false,
      acting_as: false,
      offer: false,
      init_cost: false,
      period: "3 months"
    }
  },
  {
    title: "Purchase Plan",
    details: {
      function: true,
      responsive: true,
      acting_as: true,
      offer: true,
      init_cost: false,
      period: false
    }
  }
]
</script>


<template>
  <div class="container-fluid px-5 py-5" style="background-color: #F4F4F4;">
    <h4 class="fs-2 fw-bold">Compare Plans</h4>
    <table class="table">
      <thead class="text-center text-light">
        <tr>
          <th scope="col"></th>
          <th scope="col" style="background-color: #1E2369;">Subscription Plan</th>
          <th scope="col" style="background-color: #D82B1B; ">Purchase Plan</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Function</th>
          <td>{{ plans[ 0 ].details.function ? 'O' : '-' }}</td>
          <td>{{ plans[ 1 ].details.function ? 'O' : '-' }}</td>
        </tr>
        <tr>
          <th scope="row">Responsive</th>
          <td>{{ plans[ 0 ].details.responsive ? 'O' : '-' }}</td>
          <td>{{ plans[ 1 ].details.responsive ? 'O' : '-' }}</td>
        </tr>
        <tr>
          <th scope="row">Acting As</th>
          <td>{{ plans[ 0 ].details.acting_as ? 'O' : '-' }}</td>
          <td>{{ plans[ 1 ].details.acting_as ? 'O' : '-' }}</td>
        </tr>
        <tr>
          <th scope="row">Offer</th>
          <td>{{ plans[ 0 ].details.offer ? 'O' : '-' }}</td>
          <td>{{ plans[ 1 ].details.offer ? 'O' : '-' }}</td>
        </tr>
        <tr>
          <th scope="row">Initial Cost</th>
          <td>{{ plans[ 0 ].details.init_cost ? 'O' : '-' }}</td>
          <td>{{ plans[ 1 ].details.init_cost ? 'O' : '-' }}</td>
        </tr>
        <tr>
          <th scope="row">Period</th>
          <td>{{ plans[ 0 ].details.period ? plans[ 0 ].details.period : '-' }}</td>
          <td>{{ plans[ 1 ].details.period ? plans[ 1 ].details.period : '-' }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>



<!-- <template>
  <div class="container-fluid px-5 py-5" style="background-color: #F4F4F4;">
    <h4 class="fs-2 fw-bold">Compare Plans</h4>
    <table class="table">
      <thead>
        <tr>
          <th scope="col"></th>
          <th scope="col">Subscription Plan</th>
          <th scope="col">Purchase Plan</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">one</th>
          <td>Mark</td>
          <td>Otto</td>
        </tr>
        <tr>
          <th scope="row">two</th>
          <td>Jacob</td>
          <td>Thornton</td>
        </tr>

      </tbody>
    </table>
  </div>
</template> -->



