<template>
  <div>
    <h1>Hello this is Todos</h1>
    <div v-for="(todo, index) in todos" :key="index">
      <Todoitem v-bind:todo="todo" />
    </div>
    <div id="map">
      <mapbox-map
        style="height: 400px"
        access-token="pk.eyJ1IjoiYWhtZWRidXJoYW4iLCJhIjoiY2s3cTdyM283MDBtNzNmcXA3MnJjMDE1dCJ9.xzQ-uE2RMYfuA9vcK1-gwg"
        map-style="mapbox://styles/mapbox/dark-v9"
        :center="[0, 0]"
        :zoom="1"
      >
        <mapbox-marker :lng-lat="[0, 0]"></mapbox-marker>
        <mapbox-popup :lng-lat="[10, 0]">
          <p>Hello world !</p>
        </mapbox-popup>
        <mapbox-marker :lng-lat="[-10, 0]" popup>
          <template v-slot:popup>
            <p>Hello Maps!</p>
          </template>
        </mapbox-marker>
        <mapbox-navigation-control position="bottom-right" />
      </mapbox-map>
    </div>

    <h3>Yeah</h3>
  </div>
</template>

<script>
import {
  MapboxMap,
  MapboxMarker,
  MapboxPopup
} from "@studiometa/vue-mapbox-gl";
import "mapbox-gl/dist/mapbox-gl.css";
import Todoitem from "./TodoItem";

export default {
  name: "Todo",
  components: {
    Todoitem,
    MapboxMap,
    MapboxMarker,
    MapboxPopup
  },
  props: ["todos"]
};
</script>

<style scoped>
#map {
  width: 100%;
  height: 500px;
}
</style>