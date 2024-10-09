<script setup>
import IconLogo from './icons/IconLogo.vue'
</script>

<template>
  <nav class="navigation">
    <span class="nav-logo"><IconLogo /></span>
    <ul class="nav-list">
      <li class="nav-item"><a href="about" @click.prevent="scroll('#about')">about</a></li>
      <li class="nav-item">
        <a href="skills" @click.prevent="scroll('#skills')">skills</a>
      </li>
      <li class="nav-item"><a href="contact" @click.prevent="scroll('#contact')">contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  methods: {
    scroll(target) {
      const element = document.querySelector(target)
      if (element) {
        const elementRect = element.getBoundingClientRect()
        const offset = window.scrollY + elementRect.top - 30 // 30px above the element
        window.scrollTo({
          top: offset,
          behavior: 'smooth'
        })
      }
    }
  }
}
</script>

<style scoped>
.navigation {
  margin: 0;
  padding: 1rem 5rem;
  display: flex;
  flex-direction: row;
  align-items: center;
  font-size: 16px;
}
.nav-list {
  width: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  list-style-type: none;
  justify-content: flex-end;
  gap: 2rem;
}
.nav-item {
  margin: 0;
}
.nav-item a {
  color: var(--lapis-lazuli);
}
.nav-item:hover,
.nav-item a:hover {
  color: var(--cosmic-latte);
}
.nav-logo {
  max-height: 40px;
  width: auto;
}
</style>
