<script setup>
import { ref } from 'vue'
import IntroBGPolygon from './IntroBGPolygon.vue'
import IconCat from './icons/IconCat.vue'
import IconD20 from './icons/IconD20.vue'
import IconRefresh from './icons/IconRefresh.vue'
import IconSelfPortrait from './icons/IconSelfPortrait.vue'
import IconSparkles from './icons/IconSparkles.vue'
const counter = ref(0)
</script>

<template>
  <section class="container home" id="home">
    <IntroBGPolygon />
    <div class="intro-container">
      <div class="intro-copy-container br-2">
        <h1 class="h1">Taylor Wilkinson</h1>
        <div class="intro-subtitle-container">
          <h2 id="subtitle">is a front-end developer</h2>
          <span class="subtitle-refresh" @click="counter++" data-state="clicked"
            ><IconRefresh
          /></span>
        </div>
        <p>
          If you’re looking for a creative front-end developer who is passionate about your end
          user’s experience, promoting web accessibility for all, and is excited to collaborate
          cross-functionally to build responsive and performant web experiences, then look no
          further!
        </p>
        <div id="acknowledgment">
          <p class="mb-0">
            I live and work on
            <a href="https://maps.fpcc.ca/languages" target="_blank">the unceded territories</a> of
            the xʷməθkʷəy̓əm (Musqueam), Sḵwx̱wú7mesh (Squamish), and səlilwətaɬ (Tsleil-Waututh)
            Nations, also known as Vancouver, BC.
          </p>
        </div>
      </div>
      <div class="intro-img-container">
        <img class="taylor-1" src="../assets/img/extreme-chill.png" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.intro-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  padding: 2.5rem 0;
  width: 100%;
  @media screen and (min-width: 1110px) {
    flex-direction: row;
  }
}
.intro-copy-container {
  background: var(--cosmic-latte);
  padding: 2.5rem;
  width: 100%;
  flex-direction: column;
  @media screen and (min-width: 1110px) {
    width: 50%;
    background: none;
  }
}
.intro-img-container {
  width: 100%;
  @media screen and (min-width: 1110px) {
    width: 50%;
  }
}
.taylor-1 {
  width: 100%;
  height: auto;
  @media screen and (min-width: 1110px) {
    max-width: 650px;
  }
}
.intro-subtitle-container {
  display: flex;
  flex-direction: row;
  align-items: center;

  #subtitle {
    margin-right: 0.5rem;
  }
}
.subtitle-refresh {
  svg {
    transition: all 2s;
    will-change: transform;
  }
  &[data-state='clicked'] {
    animation: loading-rotation 2s linear;
  }
}
@keyframes loading-rotation {
  100% {
    transform: rotate(365deg);
  }
}
</style>
