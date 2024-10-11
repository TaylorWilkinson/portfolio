<script setup>
import IconLogo from './icons/IconLogo.vue'
import IconLinkedIn from './icons/IconLinkedIn.vue'
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
      <li class="nav-item-icon">
        <a href="https://www.linkedin.com/in/taylorjwilkinson/" target="_blank"><IconLinkedIn /></a>
      </li>
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
  padding: 1rem 2rem;
  display: flex;
  flex-direction: row;
  align-items: center;
  font-size: 16px;
  gap: 1rem;
  @media screen and (min-width: 1110px) {
    padding: 1rem 5rem;
  }
}
.nav-list {
  width: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  list-style-type: none;
  gap: 1rem;
  @media screen and (min-width: 1110px) {
    gap: 2rem;
  }
}
.nav-item {
  margin: 0;
}
.nav-item a {
  color: var(--lapis-lazuli);
  font-weight: 300;
}
.nav-item:hover,
.nav-item a:hover {
  color: var(--cosmic-latte);
}

.nav-item-icon {
  opacity: 1;
  transition: opacity 0.35s ease-in-out;
}
.nav-item-icon:hover,
.nav-item-icon a:hover {
  opacity: 0.5;
}
.nav-logo {
  max-height: 40px;
  width: auto;
}
</style>
