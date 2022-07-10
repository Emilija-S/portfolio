<template>
  <aside>
    <h3 class="text-uppercase d-flex flex-row align-items-center justify-content-center mt-5 pt-5">Interests
      <span class="ps-3"><i @click="isActiveInterests" class="fa fa-arrow-circle-down fa-2x btn btn-danger"/></span>
    </h3>
    <hr/>
    <ul class="list-unstyled mt-3">
    <li v-if="isActiveButtonInterests" v-for="interest in interests"
        class="fs-4 text-uppercase d-flex justify-content-center text-center my-4 mx-md-5 mx-lg-3 px-md-5 px-lg-3">{{ interest }}
    </li>
    </ul>
  </aside>
</template>

<script>
export default {
  name: "Interests",
  data() {
    return {
      interests: [
        'Nature',
        'Books',
        'Traveling',
        'Cycling',
        'Tennis',
        'Fitness'
      ],
      isActiveButtonInterests: false
    }
  },
  methods: {
    isActiveInterests() {
      this.isActiveButtonInterests = !this.isActiveButtonInterests;
    }
  }
}
</script>

<style scoped>
</style>