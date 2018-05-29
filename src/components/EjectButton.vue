<template>
  <div class="eject-button">
    <span @click="$emit('eject')">EJECT</span>
  </div>
</template>

<script>
export default {
  name: 'EjectButton',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
