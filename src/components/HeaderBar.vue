<template>
  <div class="header">
    <img src="../assets/ablogo.png" alt="ab logo">
    <a v-on:click="logout">
      Logout
      <i class="fas fa-sign-out-alt"></i>
    </a>

  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
  },
  methods: {
    logout: () => {
      alert("You logged out!!");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.header {
  height: 98px;
  width: auto;
  background-color: #F4EB20;
}
</style>
