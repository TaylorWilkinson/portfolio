<template>
  <section class="container about" id="about">
    <div class="about-copy br-2">
      <h2>Hello there internet traveller!</h2>
      <p>
        I am a normal human woman (definitely not a nursery of raccoons in a human suit) that codes
        for a living. My career in web development began in 2013 when I was playing with custom CSS
        on my secret One Direction tumblr blog. Once I realized “Wow, people do this for a living!”
        (“this” being coding and web design, not reposting 2010s celeb photos), it propelled me to
        apply to SFU’s SIAT program - an interdisciplinary school that covered development, design,
        and media. I graduated in 2019 with my BSc. in Interactive Systems.
      </p>
      <p>
        Fast forward to now, I am working as a web developer in-house on a marketing team, working
        with internal stakeholders and marketers to maintain their website and manage web content. I
        still love playing with CSS to this day. Other tools and stacks I’ve used include
        Javascript, HTML5, React, Gatsby.js, Vue.js, and GraphQL.
      </p>
      <p class="mb-0">
        Outside of work, I’m a zealous Dungeons & Dragons player and game master. I’m also a cat
        parent, hobbyist photographer, astrology nerd, and music lover.
      </p>
    </div>
    <div class="about-img"><img class="circle-img" src="../assets/img/taylor.png" /></div>
  </section>
</template>

<style scoped>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
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
