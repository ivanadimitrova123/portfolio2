<template>
<section>
  <div class="row">
    <div class="col col-md-3 text-danger text-md-end col-12 text-center">{{school.schoolDegree}}</div>
    <div class="col col-md-9 text-md-start col-12 text-center">
      <p>{{school.schoolName}}</p>
    </div>
  </div>
</section>
</template>

<script>
export default {
  name: "CardForSchool",
  props: {
    school: Object
  }
}
</script>

<style scoped>

</style>