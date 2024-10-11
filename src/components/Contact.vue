<script setup>
import IconD20 from './icons/IconD20.vue'
</script>

<template>
  <section class="container contact" id="contact">
    <div class="contact-container">
      <h2>Let's get in touch!</h2>
      <p>
        Have a role you think I'm the right fit for? Want to talk about web development? Hit me up
        on
        <a href="https://www.linkedin.com/in/taylorjwilkinson/">on LinkedIn</a>!
      </p>
      <!-- TODO: Add in slide out spotify playlist -->
    </div>
  </section>
</template>

<style scoped>
.contact {
  display: flex;
}
.contact-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
