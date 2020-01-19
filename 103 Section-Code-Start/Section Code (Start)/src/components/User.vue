<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm an awesome User!</p>
    <p>Parent user name: {{name}}</p>
    <button @click="changeName">Change my Name</button>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <app-user-detail :name="name" v-on:setNewName="name = $event" :resetFn="resetName" :userAge="age"></app-user-detail>
      </div>
      <div class="col-xs-12 col-sm-6">
        <app-user-edit :userAge="age" v-on:ageWasEdited="age = $event"></app-user-edit>
      </div>
    </div>
  </div>
</template>


<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";

export default {
  data: () => ({
    name: "Olga",
    age: 27
  }),
  methods: {
    changeName() {
      this.name = "Petr";
    },
    resetName() {
      this.name = "NameFromParent";
    }
  },
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit
  }
};
</script>

<style scoped>
div {
  background-color: lightblue;
}
</style>
