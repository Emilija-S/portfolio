<template>
  <aside>
    <h3 class="text-uppercase d-flex flex-row align-items-center justify-content-center mt-5 pt-5">Education
      <span class="ps-3"><i @click="isActiveEducation" class="fa fa-arrow-circle-down fa-2x btn btn-danger"/></span>
    </h3>
    <hr/>
    <ul v-for="degree in degrees" class="list-unstyled">
    <li v-if="isActiveButtonEducation" class="d-flex justify-content-center text-center">
      <h4><i class="fa fa-graduation-cap me-2" aria-hidden="true"></i>{{ degree.degreeName }}</h4>
    </li>
    <li v-if="isActiveButtonEducation">
      <p class="fs-5 d-flex justify-content-center text-center">{{ degree.begin }} - {{ degree.end }}</p>
    </li>
    </ul>
  </aside>
</template>

<script>
export default {
  name: "Education",
  data() {
    return {
      degrees: [
        {
          degreeName: 'Degree Name 1',
          begin: 'yearX',
          end: 'yearY'
        },
        {
          degreeName: 'Degree Name 2',
          begin: 'yearZ',
          end: 'yearT'
        },
        {
          degreeName: 'Degree Name 3',
          begin: 'yearH',
          end: 'yearP'
        }
      ],
      isActiveButtonEducation: false
    }
  },
  methods: {
    isActiveEducation() {
      this.isActiveButtonEducation = !this.isActiveButtonEducation;
    }
  }
}
</script>

<style scoped>
</style>