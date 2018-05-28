<template>
  <div class="status">
    <div class="bananas">
      Bananas Left
      <div class="bananas-status">
        {{status.bananas}}
      </div>
    </div>
    <div class="oil">
      Oil Slick
      <div class="oil-status">
        <span v-if="status.oil">Ready</span>
        <span v-else>Filling Resevoir</span>
      </div>
    </div>
    <div class="spikes">
      Wheel Spikes
      <div class="spikes-status">
        <span v-if="status.spikes">Deployed</span>
        <span v-else>Retracted</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Status',
  props: {
  },
  data(){
    return {
      status:{
        bananas: 3,
        oil: true,
        spikes: false
      }
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
    display: grid;
  }
  .bananas {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 1;
  }
  .oil {
    grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 1;
    grid-row-end: 1;

  }
  .spikes {
    grid-column-start: 3;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 1;
  }
</style>
