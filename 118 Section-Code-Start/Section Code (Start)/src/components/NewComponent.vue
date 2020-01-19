<template>
  <div>
    <h3>New Quote</h3>
    <button @click="counter++">Increse</button>
    <span>Counter is {{counter}}</span>
  </div>
</template>

<script>
export default {
  data: () => ({
    counter: 0
  }),
  destroyed(){
      console.log("destroyed!!!")
  },
  deactivated(){
       console.log("deactivated!!!");
  },
    activated(){
       console.log("activated!!!");
  }
};
</script>

<style>
</style>