<template>
  <div id="map"></div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      map: {},
    }
  },
  mounted() {
    const mapboxgl = require('mapbox-gl/dist/mapbox-gl.js')

    mapboxgl.accessToken =
      'pk.eyJ1IjoiYXJpcGFkcmlhbiIsImEiOiJja2xoYnF1a24xNmtiMm9xcHdsODAzbmZuIn0.rsPD86w82iXUMRZistT3Ww'
    this.map = new mapboxgl.Map({
      container: 'map',
      style: 'mapbox://styles/mapbox/streets-v11',
      zoom: 11,
      center: [65, 95],
    })
  },
}
</script>

<style>
#map {
  width: 100%;
  height: 100vh;
}
</style>
