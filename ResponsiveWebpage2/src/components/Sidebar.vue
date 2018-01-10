<template>
  <div class='col-12 col-lg-3 bg-light sidebar-wrapper'>
    <div class='container'>
      <div class='d-inline-flex col-5 col-lg-12 mt-1 mt-lg-5 pt-lg-5'>
        <i class='fas fa-code fa-5x col-4'></i>
        <input type='button' value='Coding' class='btn btn-lg px-5 h1 font-weight-bold bg-light responsive-font-size'>
      </div>
      <div class='d-inline-flex col-5 col-lg-12 mt-1 py-1'>
        <i class='fas fa-leaf fa-5x col-4'></i>
        <input type='button' value='Environment' class='btn btn-lg px-4 font-weight-bold bg-light responsive-font-size'>
      </div>
      <div class='d-inline-flex col-5 col-lg-12 mt-1 py-1'>
        <i class='fas fa-globe fa-5x col-4'></i>
        <input type='button' value='Culture' class='btn px-5 font-weight-bold bg-light responsive-font-size'>
      </div>
      <div class='d-inline-flex col-5 col-lg-12 mt-1 py-1'>
        <i class='fas fa-list fa-5x col-4'></i>
        <input type='button' value='All' class='btn btn-lg px-5 font-weight-bold bg-light responsive-font-size'>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'sidebar',
    data() {
      return {
        filter: ''
      }
    },
  }
</script>

<style>
  .sidebar-wrapper {
    height: 100vh !important;
  }

  @media (max-width: 992px) {
    .sidebar-wrapper {
      height: 12em !important;
    }
  }

.responsive-font-size {
  font-size: 1.5vw;
}
</style>



