<template>
  <div class="spikes-button">
    <span @click="$emit('toggleSpikes')">
      <img src="../assets/spikes-icon.png" alt="Spikes Button Icon">
      <div class="button-label">
        Toggle Spikes
      </div>
    </span>
  </div>
</template>

<script>
export default {
  name: 'SpikesButton',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.spikes-button{
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 2;
  grid-row-end: 2;
}

</style>
