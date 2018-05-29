

<template>
  <div id="app">
    <div class="header-wrapper">
      <HeaderBar/>
    </div>
    <div class="status-wrapper">
      <StatusBar :status="this.store.status"/>
    </div>
    <div class="buttons-wrapper">
      <div class="buttons">
        <BananaButton v-on:tossBanana="this.store.updateBanana"/>
        <OilButton v-on:sprayOil="this.store.updateOil"/>
        <SpikesButton v-on:toggleSpikes="this.store.updateSpikes"/>
        <EjectButton v-on:eject="this.store.ejectAlert"/>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import StatusBar from './components/StatusBar.vue'
import BananaButton from './components/BananaButton.vue'
import OilButton from './components/OilButton.vue'
import SpikesButton from './components/SpikesButton.vue'
import EjectButton from './components/EjectButton.vue'

export default {
  name: 'app',
  components: {
    HeaderBar,
    StatusBar,
    BananaButton,
    OilButton,
    SpikesButton,
    EjectButton,
  },
  data() {
      return {
        store: {
          status: {
            bananas: 504,
            isOilReady: true,
            isSpikesDeployed: false
          },
          updateBanana: () => {
            this.store.status.bananas -= 1;
          },
          updateOil: () => {
            if(this.store.status.isOilReady){
              this.store.status.isOilReady = !this.store.status.isOilReady;
              setTimeout(()=>{
                this.store.status.isOilReady = !this.store.status.isOilReady;
              }, 3000);
            } else {
            }
          },
          updateSpikes: () => {
            let deployed = this.store.status.isSpikesDeployed;
            this.store.status.isSpikesDeployed = !deployed;
          },
          ejectAlert: () => {
            alert("EJECTED");
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
  color: #000000;
  font-weight: normal;
  font-weight: 800;
  font-family: 'Dosis', sans-serif;
  font-size: 120%;
}
body {
  padding: 0px;
  margin: 0px;

}

.buttons {
  background-color: #F4EB20;
  display: grid;
  padding: 30px;
  padding-top: 20px;
  max-width: 560px;
  margin: auto;
}
.buttons-wrapper {
  background-color: #F4EB20;
}
.button-label{
  font-size: 120%;
}
.header-wrapper{
  background-color: #F4EB20;

}

</style>
