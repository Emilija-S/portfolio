<template>
  <div>

    <li v-if="isActiveButtonEducation" class="d-flex justify-content-center"><h4><i class="fa fa-graduation-cap me-2" aria-hidden="true"></i>{{ educationDegree.degreeName }}</h4></li>
    <li v-if="isActiveButtonEducation"><p class="fw-normal fs-5 d-flex justify-content-center">{{ educationDegree.begin }} - {{ educationDegree.end }}</p></li>

  </div>
</template>

<script>
export default {
  name: "Education",
  props: {
    educationDegree: Object,
    isActiveButtonEducation: Boolean
  }
}
</script>

<style scoped>

</style>