<!-- <script setup>
const features = [
  {
    iconSrc: "@/assets/icon-1.svg",
    title: "Point 1",
    description: "Lorem ipsum",
  },
  {
    iconSrc: "@/assets/icon-2.svg",
    title: "Point 2",
    description: "Lorem ipsum",
  },
  {
    iconSrc: "@/assets/icon-3.svg",
    title: "Point 3",
    description: "Lorem ipsum",
  },
];
</script>
<template>
  <div class="container-fluid">
    <div class="col-sm-3">
      <img class="feature-image" src="@/assets/img-2.svg" alt="Image 2" />
    </div>
    <div class="col-sm-9 d-flex justify-content-end">
      <h4>Feature</h4>
      <figure v-for="feature in features" :key="feature.title">
        <img class="feature-image" :src="feature.iconSrc" :alt="feature.title" />
        <figcaption>
          <h4>{{ feature.title }}</h4>
          <p>{{ feature.description }}</p>
        </figcaption>
      </figure>
    </div>
  </div>
</template> -->


<script setup>
let icon1 = "@/assets/icon-1.svg"
let icon2 = "@/assets/icon-2.svg"
let icon3 = "@/assets/icon-3.svg"

const features = [
  {
    iconSrc: icon1,
    title: "Point 1",
    description: "Ea aliqua quis sit id pariatur nulla nulla aliquip.",
  },
  {
    iconSrc: icon2 ,
    title: "Point 2",
    description: "Sit culpa cupidatat eu ea mollit non eu elit eu eu.",
  },
  {
    iconSrc: icon3,
    title: "Point 3",
    description: "Ea ex ipsum pariatur laboris dolore incididunt deserunt nostrud id deserunt ex.",
  },
];
</script>

<!-- <template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-3">
        <img class="feature-image" src="@/assets/img-2.svg" alt="Image 2" />
      </div>

      <div class="col-sm-9">
        <h4 class="fs-2 fw-bold">FEATURE</h4>
        <div v-for="feature in features" :key="feature.title" class="mb-4">
          <div class="d-flex align-items-start">
            <img class="feature-image" :src="feature.iconSrc" :alt="feature.title" />
            <div class="ml-3">
              <h4>{{ feature.title }}</h4>
              <p>{{ feature.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template> -->


<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-3">
        <img class="feature-image" src="@/assets/img-2.svg" alt="Image 2" />
      </div>

      <div class="col-sm-9 ">
        <h4 class="fs-2 fw-bold my-5">FEATURE</h4>
        <div v-for="feature in features" :key="feature.title" class="mb-4 mx-5">
          <div class="d-flex align-items-center ">
            <img class="feature-image" :src="feature.iconSrc" :alt="feature.title" />
            <div class="ml-6">
              <h4>{{ feature.title }}</h4>
              <p>{{ feature.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.col-sm-3 {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.col-sm-9 {
  padding: 1rem;
  align-items: center;
}

.feature-image {
  max-width: 100%;
  max-height: 100%;
}
</style>
