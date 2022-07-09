<template>
  <section>

  <li  class="btn p-2"  :class="(currentNumberOfStars >= 1)? bgColor : ''" @click="rating(1)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
  <li  class="btn p-2"  :class="(currentNumberOfStars >= 2)? bgColor : ''" @click="rating(2)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
  <li  class="btn p-2"  :class="(currentNumberOfStars >= 3)? bgColor : ''" @click="rating(3)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
  <li  class="btn p-2"  :class="(currentNumberOfStars >= 4)? bgColor : ''" @click="rating(4)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
  <li  class="btn p-2"  :class="(currentNumberOfStars === 5)? bgColor : ''" @click="rating(5)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>

  </section>
</template>

<script>
export default {
name: "StarRating",

  methods: {
    rating(numberOfStars) {
      this.currentNumberOfStars = numberOfStars;
      this.sumOfStars += numberOfStars;
      this.ratingCounter++;
    }
  },
  computed: {
    ratioCalculated() {
      return (this.sumOfStars / this.ratingCounter).toFixed(2);
    }
  },

  data() {
    return {
      sumOfStars: 0,
      ratingCounter: 0,
      bgColor: 'bg-warning',
      currentNumberOfStars: 0
    }
  }
}
</script>

<style scoped>

</style>