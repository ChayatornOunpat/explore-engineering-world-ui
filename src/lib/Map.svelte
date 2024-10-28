<script>
  import { onMount } from 'svelte';
  import 'leaflet/dist/leaflet.css';
  import L from 'leaflet';

  let map;

  onMount(() => {
    map = L.map('map').setView([51.505, -0.09], 13);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 19,
      attribution: '© OpenStreetMap'
    }).addTo(map);

    L.marker([51.505, -0.09]).addTo(map)
      .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
      .openPopup();
  });
</script>

<style>
  #map {
    height: 400px;
    width: 100%;
  }
</style>

<div id="map" class="min-h-screen z-0"></div>
