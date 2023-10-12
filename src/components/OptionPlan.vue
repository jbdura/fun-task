<script setup>
const details = [
  {
    title: "Support Plan",
    price: "$10/month",
    details: "Lorem ipsum",
    color: "bg-primary",
  },
  {
    title: "Basic customize",
    price: "$20/month",
    details: "Lorem ipsum",
    color: "bg-success",
  },
  {
    title: "Pro customize",
    price: "$100/month",
    details: "Lorem ipsum",
    color: "bg-danger",
  },
  {
    title: "Other customize",
    price: "Contact us",
    details: "Lorem ipsum",
    color: "bg-warning",
  },
]
</script>


<template>
  <div class="container-fluid">
    <h4 class="fs-2 fw-bold">Option Plan</h4>
    <div class="row g-4">
      <div v-for="(card, index) in details" :key="index" class="col">
        <div class="d-flex justify-content-center align-items-center">
          <div class="card custom-card" style="width: 494px; height: 204px;">

            <div class="card-body ">
              <h5 class="card-title {{ card.color }}">{{ card.title }}</h5>
              <p class="card-text">{{ card.price }}</p>
              <p class="card-text">{{ card.details }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.custom-card {
  max-width: 494px;
  height: 204px;
}
</style>

<!-- <template>
  <div class="container-fluid">
    <h4 class="fs-2 fw-bold">Option Plan</h4>
    <div class="row row-cols-2 g-4">
      <div v-for="(card, index) in details" :key="index" class="col">
        <div class="card">
          <div class="{{ card.color }}">
            {{ card.title }}
          </div>
          <div class="card-body">
            <h5 class="card-title {{ card.color }}">{{ card.title }}</h5>
            <p class="card-text">{{ card.price }}</p>
            <p class="card-text">{{ card.details }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style> -->

<!-- <script setup>
const cards = [
  {
    title: "Support menu",
    price: "$10/month",
    details: "Lorem ipsum",
    color: "bg-primary",
  },
  {
    title: "Basic customize",
    price: "$20/month",
    details: "Lorem ipsum",
    color: "bg-success",
  },
  {
    title: "Pro customize",
    price: "$100/month",
    details: "Lorem ipsum",
    color: "bg-danger",
  },
  {
    title: "Other customize",
    price: "Contact us",
    details: "Lorem ipsum",
    color: "bg-warning",
  },
]
</script>

<template>
  <div class="container-fluid">
    <h4 class="fs-2 fw-bold">Option Plan</h4>
    <div class="row row-cols-2 g-4">
      <div v-for="(card, index) in cards" :key="index" class="col">
        <div class="card">
          <div class="card-header text-white {{ card.color }}">
            {{ card.title }}
          </div>
          <div class="card-body">
            <h5 class="card-title {{ card.color }}">{{ card.title }}</h5>
            <p class="card-text">{{ card.price }}</p>
            <p class="card-text">{{ card.details }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

 -->
