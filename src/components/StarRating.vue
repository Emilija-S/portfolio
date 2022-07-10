<template>
  <section>
    <h3 class="col-12 d-flex justify-content-center text-center mt-5 px-5">RATE YOUR EXPERIENCE: </h3>
    <ul class="col-12 list-unstyled d-flex flex-row justify-content-center">
      <li v-for="numberOfStars in 5" class="btn p-2" :class="(selectedNumberOfStars >= numberOfStars)? bgColor : ''"
          @click="rating(numberOfStars)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i>
      </li>
    </ul>
    <h3 v-if="firstSelect" class="col-12 d-flex justify-content-center text-center">Average rating reached: {{ ratioCalculated }}</h3>
  </section>
</template>

<script>
export default {
  name: "StarRating",
  methods: {

    rating(numberOfStars) {
      this.firstSelect = true;
      this.selectedNumberOfStars = numberOfStars;
      this.sumOfStars += numberOfStars;
      this.ratingCounter++;
    }
  },
  computed: {
    ratioCalculated() {
      return (this.sumOfStars / this.ratingCounter).toFixed(2);
    },

    isFirstSelect() {
      return this.firstSelect;
    }
  },
  data() {
    return {
      sumOfStars: 0,
      showImg: false,
      ratingCounter: 0,
      firstSelect: false,
      bgColor: 'bg-warning',
      selectedNumberOfStars: 0
    }
  }
}
</script>

<style scoped>
</style>