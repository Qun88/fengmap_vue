<template>
  <div class="hello">
    <FMap />
    <button value="Office" @click.prevent="flag=true" style="position:relative">Office</button>
    <button value="Factory" @click.prevent="flag=false" style="position:relative">Factory</button>
    <FirstMapPage v-if="flag" mapId="90870" />
    <SecondMapPage v-else mapId="90873" />
  </div>
</template>

<script>
import FirstMapPage from "./FirstMapPage";
import SecondMapPage from "./SecondMapPage";
import FMap from "./FMap";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    FMap,
    FirstMapPage,
    SecondMapPage
  },
  data: function() {
    return { flag: true };
  },
  mounted() {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#container {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
