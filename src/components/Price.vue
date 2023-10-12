<script setup>
import OptionPlan from './OptionPlan.vue';
import OperatingEnv from './OperatingEnv.vue'

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
    }
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


