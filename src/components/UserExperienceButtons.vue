<template>

  <div class="container p-5 d-flex justify-content-center">

    <button @click="isClickedLike" class="btn btn-secondary rounded rounded-pill text-white px-3 me-3 ">LIKE
      <span class="badge px-3"> {{ likesCounter }}</span>
    </button>

    <button @click="isClickedDislike" class="btn btn-danger rounded rounded-pill text-white px-3">DISLIKE
      <span class="badge px-3"> {{ dislikesCounter }}</span>
    </button>

  </div>

</template>

<script>
export default {
name: "UserExperienceButtons",

  methods: {
    isClickedLike() {
      this.likesCounter++;
    },
    isClickedDislike() {
      this.dislikesCounter++;
    }
  },

  data() {
  return {
    likesCounter: 0,
    dislikesCounter: 0
  }
  }
}
</script>

<style scoped>

</style>