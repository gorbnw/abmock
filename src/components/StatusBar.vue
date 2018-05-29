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
        <span v-else>Filling Resevoir</span>
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
    height: 50px;
    display: block;
    padding: 0px;
    margin: auto;
  }
  .bananas {
    width: 25%;
    padding: 0px;
    margin: auto;
    display: inline-block;
    /* grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 1; */
  }
  .oil {
    width: 25%;
    padding: 0px;
    margin: auto;
    display: inline-block;

    /* grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 1;
    grid-row-end: 1; */

  }
  .spikes {
    width: 25%;
    padding: 0px;
    margin: auto;
    display: inline-block;

    /* grid-column-start: 3;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 1; */
  }

  .dash-label{
  font-size: 80%;
  font-weight: normal;
  }
</style>
