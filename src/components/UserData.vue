<template>
  <form @submit.prevent="setUser">
    <label for="name">Name</label>
    <input type="text" placeholder="Name" v-model="enterName" />
    <label for="age">agge</label>
    <input type="number" placeholder="Age" v-model="enterAge" />
    <button>Set New User</button>
  </form>
</template>
<script>
export default {
  emits: ["set-user"],
  data() {
    return {
      enterName: "",
      enterAge: ""
    };
  },
  methods: {
    setUser() {
      this.$emit("set-user", this.enterName, this.enterAge);
    }
  }
};
</script>