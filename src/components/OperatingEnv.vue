<script setup>
const details = [
  {
    title: "Operating environment",
    details: [ "Lorem ipsum" ]
  },
  {
    title: "Server requirements",
    details: [
      "Apache",
      "PHP",
      "DB SQLite"
    ]
  }
]

const QA = [
  {
    Q: "Q: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
    A: "A: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  }
]
</script>


<template>
  <div class="container-fluid vh-100 ">
    <h4 class="fs-2 fw-bold">Operating Environment</h4>

    <div class="d-flex  align-items-left h-100">
      <div>
        <div v-for="(detail, index) in details" :key="index">
          <h5>{{ detail.title }}</h5>
          <ul>
            <li v-for="(item, itemIndex) in detail.details" :key="itemIndex">{{ item }}</li>
          </ul>
        </div>

        <hr class="my-5">

        <h4 class="fs-2 fw-bold">QA</h4>
        <div v-for="(item, index) in QA" :key="index">
          <p>{{ item.Q }}</p>
          <p>{{ item.A }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
