<template>
  <section>
    <h4 class="m-3 ps-2">{{ softSkill.skillName }}</h4>
    <p class="text-left fs-5">{{ softSkill.skillDescription }}</p>
  </section>
</template>

<script>
export default {
  name: "KeySkills",
  props: {
    softSkill: Object
  }
}
</script>

<style scoped>

</style>