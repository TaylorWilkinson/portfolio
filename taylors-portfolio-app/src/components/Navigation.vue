<script setup>
function scroll() {
  alert('SCROLLING')
}
</script>

<template>
  <nav class="navigation">
    <ul class="nav-list">
      <!-- <li class="nav-item"><a href="/">Taylor W</a></li> -->
      <li class="nav-item"><a href="about" @click="scroll('about')">about</a></li>
      <li class="nav-item"><a href="experience">experience</a></li>
      <li class="nav-item"><a href="contact">contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.navigation {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  margin: 0;
  padding: 0.5rem 0;
  font-size: 16px;
  .nav-list {
    display: flex;
    list-style-type: none;
    margin: 0;
    padding: 0;
  }
  .nav-item,
  .nav-item a {
    margin: 0.5rem 1rem;
    color: var(--lapis-lazuli);
  }
  .nav-item:hover,
  .nav-item a:hover {
    color: var(--cosmic-latte);
  }
  .home-item {
    margin: 0.5rem 1rem;
  }
}
</style>
