<template>
  <svg
    class="intro-bg-polygon"
    width="944"
    height="400"
    viewBox="0 0 944 400"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path d="M505.5 0H0V400H944L505.5 0Z" fill="#FFF5E0" />
  </svg>
</template>

<style scoped>
.intro-bg-polygon {
  display: none;
  opacity: 0;
  @media screen and (min-width: 1110px) {
    display: block;
    position: absolute;
    z-index: -100;
    opacity: 1;
  }
}
</style>
