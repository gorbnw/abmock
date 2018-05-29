<template>
  <div class="spikes-button">
    <span @click="$emit('toggleSpikes')">Swap Spikes</span>
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

</style>
