<script setup>
import IntroBGPolygon from './IntroBGPolygon.vue'
import IconCat from './icons/IconCat.vue'
import IconD20 from './icons/IconD20.vue'
import IconRefresh from './icons/IconRefresh.vue'
import IconSelfPortrait from './icons/IconSelfPortrait.vue'
import IconSparkles from './icons/IconSparkles.vue'
</script>

<template>
  <section class="container home mt-0" id="home">
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
            v-on:keypress="spin(), changeText()"
            aria-controls="subtitle"
            tabindex="0"
            ><IconRefresh
          /></span>
        </div>
        <p>
          If you’re looking for a creative front-end developer who is passionate about your end
          user’s experience, promoting web accessibility for all, and is excited to collaborate
          cross-functionally and build responsive and performant web experiences, then look no
          further!
        </p>
        <div id="acknowledgment">
          <p class="mb-0">
            I live and work on the unceded territories of the xʷməθkʷəy̓əm (Musqueam), Sḵwx̱wú7mesh
            (Squamish), and səlilwətaɬ (Tsleil-Waututh) Nations, also known as Vancouver, BC.
          </p>
        </div>
      </div>
      <div class="intro-img-container">
        <img
          class="taylor-1"
          src="../assets/img/extreme-chill.png"
          alt="Taylor Wilkinson wearing pink sunglasses and an all-black business-casual outfit while lying diagonally and upside-down in a black armchair, pointing her hands into finger guns pointed at the camera"
        />
        <span class="graphic-container" id="sparkles"><IconSparkles /></span>
        <span class="graphic-container" id="cat"><IconCat /></span>
        <span class="graphic-container" id="d20"><IconD20 /></span>
        <span class="graphic-container" id="self-portrait"><IconSelfPortrait /></span>
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
      }, 1000)
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
  position: relative;
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
  transition: transform 0.7s;
}
.loading {
  animation: loading-rotation 0.7s ease;
}

@keyframes loading-rotation {
  100% {
    transform: rotate(360deg);
  }
}

.graphic-container {
  transition: transform 0.75s;
  animation: pop-in 0.75s linear;
}
@keyframes pop-in {
  0% {
    transform: scale(0);
  }
  40% {
    transform: scale(1.25);
  }
  60% {
    transform: scale(1);
  }
  80% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
#sparkles,
#cat,
#d20,
#self-portrait {
  position: absolute;
}
#cat {
  top: 5%;
  right: 20%;
  @media screen and (min-width: 800px) {
    top: 15%;
    right: 22%;
  }
}
#d20 {
  top: 20%;
  left: 5%;
  @media screen and (min-width: 800px) {
    top: 0;
    left: 30%;
  }
}
#self-portrait {
  bottom: 10%;
  left: 0;
  @media screen and (min-width: 800px) {
    bottom: 25%;
    left: 20%;
  }
  @media screen and (min-width: 1110px) {
    right: -5%;
    bottom: 25%;
  }
}
#sparkles {
  right: 15%;
  bottom: 10%;
  @media screen and (min-width: 800px) {
    right: -5%;
    bottom: 45%;
  }
  @media screen and (min-width: 1110px) {
    right: -5%;
    top: 30%;
  }
}
</style>
