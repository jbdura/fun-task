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
      desc: [
        "Tempor cupidatat voluptate officia culpa laborum enim ex proident culpa eu deserunt.",
        "In ea cillum ut occaecat sint ullamco aute in qui elit mollit sint proident.",
        "Fugiat non consequat anim reprehenderit excepteur eu est aute et ea."
      ],
    },
    option: "Options",
    optionDesc: [
      "Non elit quis laborum elit id do tempor anim proident mollit id.",
      "Velit irure voluptate deserunt magna ullamco deserunt adipisicing laboris labore fugiat consequat.",
      "Sunt consectetur veniam veniam excepteur esse aliqua elit ipsum deserunt exercitation."
    ],
    color: "#000080",
    extras: {
      title: "Service provision",
      details: [
        "Labore amet magna ipsum officia laboris proident cupidatat.",
        "In exercitation irure consequat sunt exercitation ut sit excepteur eu exercitation mollit."
      ]
    },
    design: designCorner,
  },
  {
    title: "Purchase Plan",
    price: "$5/month",
    details: {
      title: "feature",
      desc: [ "Ad ipsum laboris laboris exercitation id ex et et nisi voluptate esse eiusmod.", "Ea enim laborum adipisicing ipsum magna." ]
    },
    option: "Options",
    optionDesc: [ "Magna enim aute excepteur do do reprehenderit do et ea aliqua in tempor elit exercitation.",
      "Labore nulla laboris amet sunt nisi pariatur pariatur." ],
    color: "#FF5733",
    extras: {
      title: "Caution",
      details: [
        "Do veniam officia mollit id magna in cupidatat minim nostrud sunt nostrud est veniam.",
        "Minim sint ad anim incididunt ea est exercitation incididunt.  "
      ]
    },
    design: designCorner2,
  }
];
</script>


<!-- 

<template>
  <div class="container-fluid px-5 py -5 pt-3">
    <h4 class="fs-2 fw-bold">Price</h4>

    <div class="float-end">
      <img class="feature-image z-n1" src="@/assets/img-3.svg" alt="Image 3" />
    </div>

    <div class="container z-0">
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
    </div>


    <br>
    <OptionPlan />
    <br>

    <div class="z-n1">
      <img class="feature-image " src="@/assets/img-4.svg" alt="Image 4" />
    </div>

    <OperatingEnv />
  </div>
</template>
 -->


<template>
  <div class="relative container-fluid px-5 py-5 pt-3 ">
    <div class="float-end absolute img2-cont">
      <img class="feature-image z-n1 " src="@/assets/img-3.svg" alt="Image 3" />
    </div>
    <h4 class="fs-2 fw-bold">Price</h4>

    <div class="row z-1">
      <!-- Subscription Plan Card -->
      <div class="container col-9 mb-4">
        <div class="card ">
          <div class="card-body">

            <h3 class="fs-2 text-primary">Subscription Plan</h3>
            <p class="fs-4">$5/month</p>
            <h5 class="fs-4">Features</h5>
            <ul>
              <li>Tempor cupidatat voluptate officia culpa laborum enim ex proident culpa eu deserunt.</li>
              <li>In ea cillum ut occaecat sint ullamco aute in qui elit mollit sint proident.</li>
              <li>Fugiat non consequat anim reprehenderit excepteur eu est aute ea.</li>
            </ul>
            <h5 class="fs-4">Options</h5>
            <ul>
              <li>Non elit quis laborum elit id do tempor anim proident mollit id.</li>
              <li>Velit irure voluptate deserunt magna ullamco deserunt adipisicing laboris labore fugiat consequat.</li>
              <li>Sunt consectetur veniam veniam excepteur esse aliqua elit ipsum deserunt exercitation.</li>
            </ul>
            <hr class="my-4">

            <h5 class="fs-4">Service Provision</h5>
            <ul>
              <li>Labore amet magna ipsum officia laboris proident cupidatat.</li>
              <li>In exercitation irure consequat sunt exercitation ut sit excepteur eu exercitation mollit.</li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Purchase Plan Card -->
      <div class="container col-md-10 mb-4">
        <div class="z-n1 absolute img1-cont">
          <img class="feature-image " src="@/assets/img-4.svg" alt="Image 4" />
        </div>
        <div class="card">
          <div class="card-body">

            <h3 class="fs-2 text-danger">Purchase Plan</h3>
            <p class="fs-4">$5/month</p>
            <h5 class="fs-4">Features</h5>
            <ul>
              <li>Ad ipsum laboris laboris exercitation id ex et et nisi voluptate esse eiusmod.</li>
              <li>Ea enim laborum adipisicing ipsum magna.</li>
            </ul>

            <h5 class="fs-4">Options</h5>
            <ul>
              <li>Magna enim aute excepteur do do reprehenderit do et ea aliqua in tempor elit exercitation.</li>
              <li>Labore nulla laboris amet sunt nisi pariatur pariatur.</li>
            </ul>
            <hr class="my-4">

            <h5 class="fs-4">Caution</h5>
            <ul>
              <li>Do veniam officia mollit id magna in cupidatat minim nostrud sunt nostrud est veniam.</li>
              <li>Minim sint ad anim incididunt ea est exercitation incididunt.</li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <br>
    <OptionPlan />

    <br>

    <OperatingEnv />
  </div>
</template>

<style>
.relative {
  position: relative;
}

.absolute {
  position: absolute;
}

.img1-cont {
  left: -12em;
}

.img2-cont {
  right: -20em;
}
</style> 


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

