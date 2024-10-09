<script setup>
import IntroBGPolygon from './IntroBGPolygon.vue'
import IconCat from './icons/IconCat.vue'
import IconD20 from './icons/IconD20.vue'
import IconRefresh from './icons/IconRefresh.vue'
import IconSelfPortrait from './icons/IconSelfPortrait.vue'
import IconSparkles from './icons/IconSparkles.vue'
</script>

<template>
  <section class="container home" id="home">
    <IntroBGPolygon />
    <div class="intro-container">
      <div class="intro-copy-container br-2">
        <h1 class="h1">Taylor Wilkinson</h1>
        <div class="intro-subtitle-container">
          <h2 id="subtitle">
            {{ subtitles[currentIndex].text }}
          </h2>
          <span
            class="subtitle-refresh"
            @click="spin(), changeText()"
            :class="{ loading: isLoading }"
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

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      isLoading: false,
      isFading: false,
      subtitles: [
        { text: 'is a front-end web developer' },
        { text: 'hopes you’re having a good day' },
        { text: 'is always learning' },
        { text: 'has a cat with a weird meow' },
        { text: 'is so Julia' },
        { text: 'hopes to be reincarnated as a capybara' },
        { text: 'is more than a culture hire' },
        { text: 'believes in you' },
        { text: 'loves Dungeons & Dragons' },
        { text: 'has a pun for that' },
        { text: 'would like to thank all women' },
        { text: 'is a Taurus Sun, Aries Moon, Cancer Rising' },
        { text: 'wants to hear about your pet' }
      ]
    }
  },
  methods: {
    changeText() {
      if (this.currentIndex === this.subtitles.length - 1) {
        this.currentIndex = 0
      } else {
        this.currentIndex++
      }
    },
    spin() {
      this.isLoading = true
      // Remove the loading class after the animation ends
      setTimeout(() => {
        this.isLoading = false
      }, 500)
    }
  }
}
</script>

<style scoped>
.intro-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  padding: 2.5rem;
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
  transition: transform 0.5s;
  will-change: transform;
}
.loading {
  animation: loading-rotation 0.5s linear;
}

@keyframes loading-rotation {
  100% {
    transform: rotate(360deg);
  }
}
</style>
