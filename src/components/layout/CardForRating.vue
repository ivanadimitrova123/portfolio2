<template>
<section>
  <div class="row">
    <div class="col col-md-3 text-danger text-md-end col-12 text-center">{{rate.rateFor}}</div>
    <div class="col col-md-9 text-md-start col-12 text-center">
      <span>{{ rate.clickText }}</span>

    </div>
  </div>
</section>
</template>

<script>
export default {
name: "CardForRating",
  props: {
    rate: Object
  }
}
</script>

<style scoped>

</style>