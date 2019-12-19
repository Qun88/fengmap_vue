<template>
  <div id="FirstMapPage">
    <button @click="openMap()" style="position:relative">Open:90870</button>
  </div>
</template>

<script>
export default {
  name: "FirstMapPage",
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

<style scoped>
</style>