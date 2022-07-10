<template>
  <section>
    <h3 class="mx-3 mt-4 text-uppercase">Soft Skills</h3>
    <hr class="mb-3"/>
    <div v-for="softSkill in softSkills">
      <h4 class="m-3 ps-2">{{ softSkill.skillName }}</h4>
      <p class="text-left fs-5">{{ softSkill.skillDescription }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "KeySkills",
  data() {
    return {
      softSkills: [
        {
          skillName: 'Excellent Communicator',
          skillDescription: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book.'
        },
        {
          skillName: 'Team Player',
          skillDescription: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book.'
        }
      ]
    }
  },
  props: {
    softSkill: Object
  }
}
</script>

<style scoped>
</style>