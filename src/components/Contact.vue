<script>
export default {
  data () {
    return {
      isFormValid: false,
    };
  },
  computed: {
    isFormValid () {
      // Implement validation logic for required fields here
      return false; // Set to true when the form is valid
    },
  },
  methods: {
    submitForm () {
      if ( this.isFormValid ) {
        // Process the form data
        this.$refs.contactForm.submit();
      }
    },
  },
};
</script>


<template>
  <div class="container-fluid px-5 py-5">
    <h2 class="text-center">Contact</h2>
    <form @submit.prevent="submitForm" ref="contactForm">
      <div class="row">
        <div class="row">
          <div class="col">
            <label for="companyName" class="form-label">Company Name:</label>
            <input type="text" class="form-control" id="companyName">
          </div>
          <div class="col">

            <label for="name" class="form-label">Name:<span class="text-danger">*</span></label>
            <input type="text" class="form-control" id="name" required>
          </div>
        </div>
        <div class="row">
          <div class="col">
            <label for="email" class="form-label">Email:<span class="text-danger">*</span></label>
            <input type="email" class="form-control" id="email" required>
          </div>
          <div class="col">
            <label for="tel" class="form-label">Tel:<span class="text-danger">*</span></label>
            <input type="tel" class="form-control" id="tel" required>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2">
            <label for="zipCode" class="form-label">Zip Code:<span class="text-danger">*</span></label>
            <input type="text" class="form-control" id="zipCode" required>

          </div>
        </div>
        <div class="row">
          <div class="col">
            <label for="prefecture" class="form-label">Prefecture:<span class="text-danger">*</span></label>
            <input type="text" class="form-control" id="prefecture" required>
          </div>
          <div class="col">
            <label for="street" class="form-label">Street:<span class="text-danger">*</span></label>
            <input type="text" class="form-control" id="street" required>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2">
            <label for="building" class="form-label">Building:</label>
            <input type="text" class="form-control" id="building">
          </div>
        </div>
        
        <div class="mb-3">
            <label class="form-label">Order Contents:<span class="text-danger">*</span></label>
            <div class="d-flex">
              <div class="form-check me-3">
                <input type="radio" class="form-check-input" id="both" name="orderContents" value="both" required>
                <label class="form-check-label" for="both">Both</label>
              </div>
              <div class="form-check me-3">
                <input type="radio" class="form-check-input" id="mainOnly" name="orderContents" value="mainOnly" required>
                <label class="form-check-label" for="mainOnly">Main Only</label>
              </div>
              <div class="form-check">
                <input type="radio" class="form-check-input" id="optionOnly" name="orderContents" value="optionOnly" required>
                <label class="form-check-label" for="optionOnly">Option Only</label>
              </div>
            </div>
          </div>
        <div class="col-sm-3">
          <label for="goods" class="form-label">Goods:<span class="text-danger">*</span></label>
          <select class="form-select" id="goods" required>
            <option value=""></option>
            <!-- Add your options here -->
          </select>
        </div>
        <div class="mb-3">
          <label for="orderDetails" class="form-label">Order Details:</label>
          <textarea class="form-control" id="orderDetails"></textarea>
        </div>
      </div>
      <div class="text-center mt-3">
        <button type="submit" class="btn btn-primary" :disabled="!isFormValid">Submit</button>
      </div>
    </form>
  </div>
</template>




<!-- 
  <div class="row">
  <div class="col">
    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
  </div>
<div class="col">
    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
  </div>
</div> 
-->