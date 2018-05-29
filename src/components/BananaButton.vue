<template>
  <div class="banana-button">
    <span @click="tossBanana">Toss Banana</span>
  </div>
</template>

<script>
export default {
  name: 'BananaButton',
  methods: {
    tossBanana: () => {
      alert("Banana tossed");
    }
  },
  props: {
    bananas: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
