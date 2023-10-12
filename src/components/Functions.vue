<script setup>
const details = [
  {
    title: "Function 1",
    desc: "Lorem ipsum"
  },
  {
    title: "Function 2",
    desc: "Lorem ipsum"
  },
  {
    title: "Function 3",
    desc: "Lorem ipsum"
  }
]
</script>



<!-- <template>
  <div class="container-fluid bg-light">
    <h4 class="fs-2 fw-bold">Function</h4>
    <div class="d-flex flex-wrap">
      <div class="card mb-3 mr-3" style="width: 18rem;" v-for="(detail, index) in details" :key="index">
        <div class="card-body">
          <h5 class="card-title">{{ detail.title }}</h5>
          <p class="card-text">{{ detail.desc }}</p>
          <a href="#" class="btn btn-warning">Go somewhere</a>
        </div>
      </div>
    </div>
  </div>
</template> -->

<template>
  <div class="container-fluid bg-light p-5">
    <h4 class="fs-2 fw-bold ">Function</h4>
    <div class="d-flex flex-wrap justify-content-center gap-5"> <!-- Center the cards -->
      <div class="card mb-5 mr-7" style="width: 18rem;" v-for="(detail, index) in details" :key="index">
        <div class="card-body">
          <h5 class="card-title">{{ detail.title }}</h5>
          <p class="card-text">{{ detail.desc }}</p>
          <a href="#" class="btn btn-warning">Go somewhere</a>
        </div>
      </div>
    </div>
  </div>
</template>











