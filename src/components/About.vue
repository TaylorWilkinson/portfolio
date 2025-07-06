<template>
  <section class="container about" id="about">
    <div class="about-container">
      <div class="about-copy br-2">
        <h2>Hello there, internet traveller!</h2>
        <p>
          I am a normal human woman (definitely not a passel of possums in a human suit) that writes
          codes for a living. My career in web development began in the 2010s when I was playing
          with custom CSS on my secret fandom tumblr blog. Once I realized “Wow, people do this for
          a living!” (“this” being development and web design, not reposting 2010s celebrity
          photos), it propelled me to apply to SFU’s SIAT program - an interdisciplinary school that
          covered development, design, and media. I graduated in 2019 with my BSc. in Interactive
          Systems.
        </p>
        <p>
          Fast forward to now, I'm working as a web developer with 5+ years of experience working
          for engineering and marketing teams alike. And yes, I still love playing with CSS to this
          day.
        </p>
        <p class="mb-0">
          Outside of work, I’m a zealous Dungeons & Dragons player and game master. I’m also a cat
          parent, hobbyist photographer, astrology nerd, and music lover.
        </p>
      </div>
      <div class="about-img">
        <img
          class="circle-img"
          src="../assets/img/taylor.png"
          loading="lazy"
          alt="Profile picture of Taylor Wilkinson"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  padding: 2.5rem 0;
  width: 100%;
  @media screen and (min-width: 1110px) {
    flex-direction: row;
  }
}
.about-copy {
  background: var(--cosmic-latte);
  padding: 2rem;
  @media screen and (min-width: 1110px) {
    flex-grow: 0;
    flex-shrink: 0;
    flex-basis: 50%;
  }
}
.circle-img {
  width: auto;
  height: auto;
}
</style>
