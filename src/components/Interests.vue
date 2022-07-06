<template>
    <li class="display-6 mb-3 d-flex"><i class="fa fa-asterisk mx-2 " aria-hidden="true"></i>{{ interest }}</li>
</template>

<script>
export default {
  name: "Interests",
  props: {
    interest: String
  }
}
</script>

<style scoped>

</style>