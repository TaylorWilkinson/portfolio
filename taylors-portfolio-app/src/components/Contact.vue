<script setup>
import SpotifyPlayer from './SpotifyPlayer.vue'
</script>

<template>
  <section class="container contact" id="contact">
    <div class="spotify-container">
      <h2>Where we dropping?</h2>
      <div class="spotify-container">
        <SpotifyPlayer />
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  margin: 2rem 0;
  display: flex;
}
.spotify-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
