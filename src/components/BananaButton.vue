<template>
  <div class="banana-button">
    <span @click="$emit('tossBanana')">Toss Banana</span>
  </div>
</template>

<script>
export default {
  name: 'BananaButton',
  props: {
    bananas: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
