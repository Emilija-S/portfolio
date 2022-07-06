<template>
  <section>

    <li class="display-6 mb-3">{{ proffesionalSkillBackend.skillName }}</li>
    <li>
      <i v-for="i in proffesionalSkillBackend.rating" class="fa fa-star fa-2x" aria-hidden="true"></i>
      <i v-for="i in 5 - proffesionalSkillBackend.rating" class="fa fa-star-o fa-2x" aria-hidden="true"></i>
    </li>

  </section>
</template>

<script>
export default {
  name: "ProffesionalSkillsBackend",
  props: {
    proffesionalSkillBackend: Object
  }
}
</script>

<style scoped>

</style>