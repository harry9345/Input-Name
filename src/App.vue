<template>
  <section>
    <active-user :username="user.name" :userage="user.age"></active-user>
    <user-data @set-user="setNewUser"></user-data>
  </section>
</template>
<script>
export default {
  data() {
    return {
      user: {
        name: "harry",
        age: 37
      }
    };
  },
  methods: {
    setNewUser(name, age) {
      this.user = {
        name: name,
        age: +age
      };
    }
  }
};
</script>



<style>
html {
  font-family: sans-serif;
}

section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid rgb(62, 52, 242);
  padding: 1rem;
}
input {
  border: 1px solid rgb(62, 52, 242);
}
</style>