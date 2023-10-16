<script setup>
let design1 = `<svg width="44" height="31" viewBox="0 0 44 31" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0.571777 0.709961H43.0874L0.571777 30.71V0.709961Z" fill="#2A8B4B"/>
</svg>
`
let design2 = `<svg width="43" height="31" viewBox="0 0 43 31" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0.337402 0.709961H42.853L0.337402 30.71V0.709961Z" fill="#CE286F"/>
</svg>
`
let design3 = `<svg width="44" height="31" viewBox="0 0 44 31" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0.571777 0.709961H43.0874L0.571777 30.71V0.709961Z" fill="#1FA6B2"/>
</svg>
`
let design4 = `<svg width="43" height="31" viewBox="0 0 43 31" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0.337402 0.709961H42.853L0.337402 30.71V0.709961Z" fill="#EA7A15"/>
</svg>
`

const details = [
  {
    title: "Support Plan",
    price: "$10/month",
    details: "Sunt dolore laboris anim ea consectetur occaecat tempor velit culpa deserunt exercitation sint.",
    design: design1 
  },
  {
    title: "Basic customize",
    price: "$20/month",
    details: "Proident consectetur Lorem irure proident enim quis.",
    design: design2
    },
  {
    title: "Pro customize",
    price: "$100/month",
    details: "Eu cillum ipsum velit cupidatat anim cillum veniam incididunt.",
    design: design3
    },
  {
    title: "Other customize",
    price: "Contact us",
    details: "Labore dolor laboris adipisicing incididunt tempor aliqua labore minim nostrud labore.",
    design: design4
  },
]
</script>



<template>
  <div class="container-fluid">
    <h4 class="fs-2 fw-bold">Option Plan</h4>
    <div class="row g-4">
      <div v-for="(card, index) in details" :key="index" class="col">
        <div class="d-flex justify-content-center align-items-center position-relative">
          <div class="card custom-card" style="width: 494px; height: 204px;">
            <!-- SVG design in top left corner -->
            <div v-html="card.design" class="position-absolute" style="top: 0; left: 0;"></div>

            <div class="card-body ">
              <h5 class="card-title">{{ card.title }}</h5>
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
