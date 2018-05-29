<template>
  <div class="status">
    <div class="bananas">
      <span class="dash-label">Bananas</span>
      <div class="bananas-status">
        {{this.status.bananas}}
      </div>
    </div>
    <div class="oil">
      <span class="dash-label">Oil Slick</span>
      <div class="oil-status">
        <span v-if="this.status.isOilReady">Ready</span>
        <span v-else>Refilling</span>
      </div>
    </div>
    <div class="spikes">
      <span class="dash-label">Wheel Spikes</span>
      <div class="spikes-status">
        <span v-if="this.status.isSpikesDeployed">Deployed</span>
        <span v-else>Retracted</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Status',
  props: {
    status:{
      bananas: Number,
      isOilReady: Boolean,
      isSpikesDeployed: Boolean,
    }
  },
  methods: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .status {
    background-color: white;
    display: block;
    height: 55px;
    padding: 0px;
    margin: auto;
    max-width: 560px;
  }
  .bananas {
    display: inline-block;
    margin: auto;
    padding: 0px;
    width: 30%;
  }
  .oil {
    display: inline-block;
    margin: auto;
    padding: 0px;
    width: 30%;
  }
  .spikes {
    display: inline-block;
    margin: auto;
    padding: 0px;
    width: 30%;
  }
  .dash-label{
  font-size: 80%;
  font-weight: normal;
  }
</style>
