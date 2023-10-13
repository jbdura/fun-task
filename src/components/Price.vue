<script setup>
import OptionPlan from './OptionPlan.vue';
import OperatingEnv from './OperatingEnv.vue'

let designCorner = `<svg width="44" height="31" viewBox="0 0 44 31" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0.498535 0.709961H43.0142L0.498535 30.71V0.709961Z" fill="#1E2369"/>
</svg>
`
let designCorner2 = `<svg width="1814" height="8400" viewBox="0 0 1814 8400" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M1814 0H0V8400H1814V0Z" fill="white"/>
</svg>
`

const prices = [
  {
    title: "Subscription Plan",
    price: "$5/month",
    details: {
      title: "feature",
      desc: [ "lorem ipsum something", "lorem ipsum something", "lorem ipsum something" ],
    },
    option: "Options",
    optionDesc: [ "lorem ipsum ipsum some some thinggg", "lorem ipsum something", "lorem ipsum something" ],
    color: "#000080",
    extras: {
      title: "Service provision",
      details: [
        "lorem ipsum",
        "lorem ipsum"
      ]
    },
    design: designCorner,
  },
  {
    title: "Purchase Plan",
    price: "$5/month",
    details: {
      title: "feature",
      desc: [ "lorem ipsum something", "lorem ipsum ipsum some some thinggg" ]
    },
    option: "Options",
    optionDesc: [ "lorem ipsum ipsum some some thinggg", "lorem ipsum something", "lorem ipsum something" ],
    color: "#FF5733",
    extras: {
      title: "Caution",
      details: [
        "lorem ipsum",
        "lorem ipsum"
      ]
    },
    design: designCorner2,
  }
];
</script>




<template>
  <div class="container-fluid px-5 py -5 pt-3">
    <h4 class="fs-2 fw-bold">Price</h4>
    <div class="container">
      <div v-for="(price, index) in prices" :key="index" class="container mb-4">
        
        <h3 class="fs-2" :style="{ color: price.color }">{{ price.title }}</h3>
        <div>
          <h4>{{ price.price }}</h4>
          <h5>{{ price.details.title }}</h5>
          <ul>
            <li v-for="(desc, descIndex) in price.details.desc" :key="descIndex">{{ desc }}</li>
          </ul>
        </div>
        <h5>{{ price.option }}</h5>
        <ul>
          <li v-for="(optionDesc, optionIndex) in price.optionDesc" :key="optionIndex">{{ optionDesc }}</li>
        </ul>

        <hr class="my-4">

        <h4>{{ price.extras.title }}</h4>
        <ul>
          <li v-for="(detail, detailIndex) in price.extras.details" :key="detailIndex">{{ detail }}</li>
        </ul>
      </div>
    </div>
    <br>
    <OptionPlan />
    <br>
    <OperatingEnv />
  </div>
</template>




<!-- <template>
  <div class="container-fluid px-5 py-5 pt-3">
    <h4 class="fs-2 fw-bold">Price</h4>
    <div class="container">
      <div v-for="(price, index) in prices" :key="index" class="container mb-4">
        <div v-html="price.design" class="position-absolute" style="top: 0; left: 0;"></div>
        <h3 class="fs-2" :style="{ color: price.color }">{{ price.title }}</h3>
        <div>
          <h4>{{ price.price }}</h4>
          <h5>{{ price.details.title }}</h5>
          <ul>
            <li v-for="(desc, descIndex) in price.details.desc" :key="descIndex">{{ desc }}</li>
          </ul>
        </div>
        <h5>{{ price.option }}</h5>
        <ul>
          <li v-for="(optionDesc, optionIndex) in price.optionDesc" :key="optionIndex">{{ optionDesc }}</li>
        </ul>

        <hr class="my-4">

        <h4>{{ price.extras.title }}</h4>
        <ul>
          <li v-for="(detail, detailIndex) in price.extras.details" :key="detailIndex">{{ detail }}</li>
        </ul>
      </div>
    </div>
    <br>
    <OptionPlan />
    <br>
    <OperatingEnv />
  </div>
</template>
 -->
