<script setup>
import SpotifyPlayer from './SpotifyPlayer.vue'
</script>

<template>
  <section class="container" id="contact">
    <div class="contact-container">
      <h2>Where we dropping?</h2>
      <SpotifyPlayer />
    </div>
  </section>
</template>

<style scoped>
.contact-container {
  margin: 2rem 0 5rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
