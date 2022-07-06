<template>
  <section>

    <li class="fs-1 mb-3 d-flex justify-content-center">{{ proffesionalSkill.skillName }}</li>
    <li class="d-flex justify-content-center">
      <i v-for="i in proffesionalSkill.rating" class="fa fa-star fa-2x" aria-hidden="true"></i>
      <i v-for="i in 5 - proffesionalSkill.rating" class="fa fa-star-o fa-2x" aria-hidden="true"></i>
    </li>

  </section>
</template>

<script>
export default {
  name: "ProffesionalSkills",
  props: {
    proffesionalSkill: Object
  }
}
</script>

<style scoped>

</style>