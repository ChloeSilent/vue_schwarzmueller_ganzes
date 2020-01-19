<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>User name: {{name}} || {{switchName()}}</p>
    <button @click="resetName">Reset name</button>
    <button @click="resetFn()">Reset name from Parent</button>
    <p>User age: {{userAge}} </p>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
      default: "Susliki"
    },
    resetFn: Function,
    userAge: Number
  },
  methods: {
    switchName() {
      return this.name
        .split("")
        .reverse()
        .join("");
    },
    resetName() {
        this.name = "a new name from child";
        this.$emit("setNewName",this.name );
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightcoral;
}
</style>
