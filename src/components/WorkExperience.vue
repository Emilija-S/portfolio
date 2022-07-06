<template>
  <section>
    <h4 class="mx-3">{{ workExperience.title }}</h4>
    <p class="mx-3 fs-6">{{ workExperience.begin }} - {{ workExperience.end }}</p>
    <p class="fs-5">
      {{ workExperience.paragraph }}
    </p>
    <p class="mx-3 fs-5 fw-bolder">Technologies used</p>
    <ul class="list-inline mb-3">
      <li class="list-inline-item m-2" v-for="experience in workExperience.technologiesUsed">
        <span class="badge bg-secondary badge-pill fs-5">
          {{ experience }}
        </span>
      </li>
    </ul>
    <hr class="hr-dashed">

  </section>
</template>

<script>
export default {
  name: "WorkExperience",
  props: {
    workExperience: Object
  }

}
</script>

<style scoped>

.hr-dashed {
  border-top: 2px dotted;
  background: white;
}

</style>