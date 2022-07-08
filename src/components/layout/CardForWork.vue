<template>
<section>
  <div class="row">
    <div class="col col-md-3 text-danger text-md-end col-12 text-center"> {{ experience.role }}</div>
    <div class="col col-md-9 text-md-start col-12 text-center">
      <p class="company"> {{ experience.companyName }} </p>
      <ul>
        <li> {{ experience.workDone1 }} </li>
        <li> {{ experience.workDone2 }} </li>
        <li> {{ experience.workDone3 }} </li>
      </ul>
    </div>
  </div>
</section>
</template>

<script>
export default {
  name: 'CardForWork',
  props: {
    experience: Object
  }
}
</script>

<style scoped>
</style>