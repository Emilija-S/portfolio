<template>
  <section>

    <li class="display-6 mb-3">{{ proffesionalSkillFrontend.skillName }}</li>
    <li>
      <i v-for="i in proffesionalSkillFrontend.rating" class="fa fa-star fa-2x" aria-hidden="true"></i>
      <i v-for="i in 5 - proffesionalSkillFrontend.rating" class="fa fa-star-o fa-2x" aria-hidden="true"></i>
    </li>

  </section>
</template>

<script>
export default {
  name: "ProffesionalSkillsFrontend",
  props: {
    proffesionalSkillFrontend: Object
  }
}
</script>

<style scoped>

</style>