<template>
  <div class="oil-button">
    <span @click="$emit('sprayOil')">Spray Oil</span>
  </div>
</template>

<script>
export default {
  name: 'OilButton',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
