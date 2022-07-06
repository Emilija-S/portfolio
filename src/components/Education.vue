<template>
  <div>

    <li class="d-flex justify-content-center"><h3><i class="fa fa-graduation-cap me-2" aria-hidden="true"></i>{{ educationDegree.degreeName }}</h3></li>
    <li><p class="fw-normal fs-5 d-flex justify-content-center">{{ educationDegree.begin }} - {{ educationDegree.end }}</p></li>

  </div>
</template>

<script>
export default {
  name: "Education",
  props: {
    educationDegree: Object
  }
}
</script>

<style scoped>

</style>