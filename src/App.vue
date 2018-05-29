

<template>
  <div id="app">
    <HeaderBar/>
    <StatusBar :status="this.store.status"/>
    <BananaButton v-on:tossBanana="this.store.updateBanana"/>
    <OilButton v-on:sprayOil="this.store.updateOil"/>
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import StatusBar from './components/StatusBar.vue'
import BananaButton from './components/BananaButton.vue'
import OilButton from './components/OilButton.vue'


export default {
  name: 'app',
  components: {
    HeaderBar,
    StatusBar,
    BananaButton,
    OilButton,
  },
  data() {
      return {
        store: {
          status: {
            bananas: 234,
            isOilReady: true,
            isSpikesDeployed: false
          },
          updateBanana: () =>{
            this.store.status.bananas -= 1;
          },
          updateOil: () =>{
            if(this.store.status.isOilReady){
              this.store.status.isOilReady = !this.store.status.isOilReady;
              setTimeout(()=>{
                this.store.status.isOilReady = !this.store.status.isOilReady;
              }, 3000);
            } else {
            }
          }
        }
      }
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
