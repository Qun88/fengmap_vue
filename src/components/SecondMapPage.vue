<template>
  <div id="SecondMapPage">
    <button @click="openMap()" style="position:relative">Open:90873</button>
  </div>
</template>

<script>
export default {
  name: "SecondMapPage",
  props: {
    mapId: String
  },
  methods: {
    openMap() {
      this.$parent.$children[0].changeMap(this.mapId);
    }
  }
};
</script>

<style  scoped>
</style>