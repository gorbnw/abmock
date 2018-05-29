<template>
  <div class="eject-button">
    <span @click="$emit('eject')">
      <img src="../assets/eject-icon.png" alt="Eject Button Icon">
      EJECT
    </span>
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

.eject-button{
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 2;
  grid-row-end: 2;
}

</style>
