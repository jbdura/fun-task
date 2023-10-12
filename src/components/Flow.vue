<script setup>
import step1 from '@/assets/step-1.svg';
import step2 from '@/assets/step-2.svg';
import step3 from '@/assets/step-3.svg';

const steps = [
  {
    icon: step1,
    step: "Step 1",
    desc: [
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      "iLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.psum"
    ]
  },
  {
    icon: step2,
    step: "Step 2",
    desc: [
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
    ]
  },
  {
    icon: step3,
    step: "Step 3",
    desc: [
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
    ]
  }
]
</script>


<template>
  <div class="container-fluid px-5 py-5">
    <h4 class="fs-2 fw-bold">Flow</h4>
    <div class="mx-auto " style="width: 600px;">
      <div v-for="(step, index) in steps" :key="index">
        <div class="d-flex align-items-center">
          <img :src="`@/assets/${step.icon}`" alt="Step Icon" />
          <div>
            <h5>{{ step.step }}</h5>
            <ul>
              <li v-for="(item, itemIndex) in step.desc" :key="itemIndex">{{ item }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <div>
      <img class="float-end" src="@/assets/img-10.svg" alt="Image 1" />
    </div>
  </div>
</template>


<!-- <template>
  <div class="container-fluid px-5 py-5">
    <h4 class="fs-2 fw-bold">Flow</h4>

  </div>
</template> -->
