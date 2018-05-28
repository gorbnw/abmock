<template>
  <div id="app">
    <HeaderBar/>
    <StatusBar/>
    <BananaButton/>
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import StatusBar from './components/StatusBar.vue'
import BananaButton from './components/BananaButton.vue'


export default {
  name: 'app',
  components: {
    HeaderBar,
    StatusBar,
    BananaButton,
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  padding: 0px;
  margin: 0px;
}
</style>
