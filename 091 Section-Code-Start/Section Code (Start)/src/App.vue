<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <h1>Components {{item}}</h1>
      </div>
      <app-server/>
    </div>
  </div>
</template>

<script>
export default {
  data: () =>({
    item: "hohoho111"
  })
};
</script>

<style>
</style>
