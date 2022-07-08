<template>
  <section>
    <div class="row">
      <div class="col col-md-3 text-danger text-md-end col-12 text-center"> {{ rate.rateFor }}</div>
      <div class="col col-md-9 text-md-start col-12 text-center d-md-flex flex-md-row">
        <p> {{ rate.clickText }} </p>
        <i role="button" @click="increaseCounterInParent" class="fa fa-star-o fa-2x ms-1" aria-hidden="true"></i>
        <span class="ms-1"> {{ counterStars }} </span>
        <span class="d-flex flex-row justify-content-md-start justify-content-center">
            <span v-for=" i in counterStars ">
              <i class="fa fa-star" aria-hidden="true"></i>
            </span>
        </span>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "CardForRating",
  props: {
    rate: Object,
    variable: Number
  },
  data() {
    return {
      counterStars: 0
    }
  },
  methods: {
    increaseCounterInParent() {
      this.counterStars++;
      if ( this.counterStars === 6 ) {
        this.counterStars -= 6;
        this.variable -= 6
      }
      this.$emit('updateCounter', this.variable + 1)
    }
  }
}
</script>

<style scoped>

</style>