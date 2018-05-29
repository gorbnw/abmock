<template>
  <div class="banana-button">
    <span @click="$emit('tossBanana')">
      <img src="../assets/banana-icon.png" alt="Banana Button Icon">
      Toss Banana
    </span>
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

.banana-button {
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 1;
  grid-row-end: 1;
}

</style>
