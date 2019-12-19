<template>
  <div id="FMap">
    <div id="container"></div>
  </div>
</template>

<script>
import fengmap from "fengmap";
var _map;

export default {
  name: "FMap",
  mounted() {
    this.initinalization("90870");
  },
  methods: {
    changeMap(mapId) {
      this.initinalization(mapId);
    },
    initinalization(mapId) {
      if (_map) {
        _map.dispose();
        _map = null;
      }

      _map = new fengmap.FMMap({
        container: document.getElementById("container"),
        appName: "蜂鸟研发SDK_2_0",
        key: "57c7f309aca507497d028a9c00207cf8",
        defaultViewMode: fengmap.FMViewMode.MODE_2D
      });
      _map.openMapById(mapId);
      _map.on("loadComplete", function() {
        alert(mapId + ' loadCompleted.');
      });
      return _map;
    }
  }
};
</script>

<style scoped>
#container {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
}
</style>
