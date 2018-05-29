<template>
  <div class="header">
    <img src="../assets/ablogo.png" alt="Logo">
    <div class="logout">
      <a v-on:click="logout">
        Log Out
        <i class="fas fa-sign-out-alt"></i>
      </a>
    </div>
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
  background-color: #F4EB20;
  height: 70px;
  padding-top: 10px;
  margin: auto;
  max-width: 560px;
  /* background-color: red; */
}

.header img{
  float: left;
  margin-left: 8%;
}

.logout {
  float: right;
  font-weight: normal;
  margin-top: 18px;
  margin-right: 5%;

}
</style>
