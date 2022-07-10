<template>
  <aside>
    <h3 class="text-uppercase d-flex justify-content-center">Professional Skills</h3>
    <hr/>
    <h4 class="mt-2 ms-5 text-decoration-underline">Frontend</h4>
    <ul v-for="professionalSkill in professionalSkillsFrontend" class="list-unstyled mt-3">
      <li class="fs-1 mb-3 d-flex justify-content-center">{{ professionalSkill.skillName }}</li>
      <li class="d-flex justify-content-center">
        <i v-for="ratingCount in professionalSkill.rating" class="fa fa-star fa-2x" aria-hidden="true"></i>
        <i v-for="ratingCount in 5 - professionalSkill.rating" class="fa fa-star-o fa-2x" aria-hidden="true"></i>
      </li>
    </ul>
    <h4 class="mt-4 ms-5 text-decoration-underline">Backend</h4>
    <ul v-for="professionalSkill in professionalSkillsBackend" class="list-unstyled mt-3">
      <li class="fs-1 mb-3 d-flex justify-content-center">{{ professionalSkill.skillName }}</li>
      <li class="d-flex justify-content-center">
        <i v-for="ratingCount in professionalSkill.rating" class="fa fa-star fa-2x" aria-hidden="true"></i>
        <i v-for="ratingCount in 5 - professionalSkill.rating" class="fa fa-star-o fa-2x" aria-hidden="true"></i>
      </li>
    </ul>
  </aside>
</template>
<script>

export default {
  name: "ProfessionalSkills",
  data() {
    return {
      professionalSkillsFrontend: [
        {
          skillName: 'HTML',
          rating: 4
        },
        {
          skillName: 'CSS',
          rating: 4
        },
        {
          skillName: 'BOOTSTRAP',
          rating: 5
        }
      ],
      professionalSkillsBackend: [
        {
          skillName: 'PYTHON',
          rating: 4
        },
        {
          skillName: 'DJANGO',
          rating: 3
        },
        {
          skillName: 'JAVA',
          rating: 5
        }
      ]
    }
  }
}
</script>

<style scoped>
</style>