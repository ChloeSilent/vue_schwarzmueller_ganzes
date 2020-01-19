<template>
  <div class="block">
    <p>Server status: {{ status }}</p>
    <button @click="changeStatus">changeStatus</button>
  </div>
</template>

<script>
export default {
  data: () => ({
    status: "critical"
  }),
  methods: {
    changeStatus() {
      if (this.status === "critical") {
        this.status = "normal";
      } else {
        this.status = "critical";
      }
    }
  }
};
</script>

<style scoped>
div {
  display: flex;
  background-color: blue;
  padding: 20px;
  margin: 10px;
  width: 200px;
}

.block p {
    color: white;
    font-weight:500;
}
</style>