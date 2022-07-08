<template>

    <li v-if="isActiveButtonInterests" class="fs-4 text-uppercase d-flex justify-content-center my-4 mx-md-5 mx-lg-3 px-md-5 px-lg-3">
      <i class="fa fa-asterisk" aria-hidden="true"></i> {{ interest }}
    </li>

</template>

<script>
export default {
  name: "Interests",
  props: {
    interest: String,
    isActiveButtonInterests: Boolean
  }
}
</script>

<style scoped>
</style>