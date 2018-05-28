<template>
  <div class="banana-button">
    <span @click="tossBanana">Toss Banana</span>
  </div>
</template>

<script>
export default {
  name: 'BananaButton',
  props: {
  },
  methods: {
    tossBanana: () =>{
      alert("Banana Tossed");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
