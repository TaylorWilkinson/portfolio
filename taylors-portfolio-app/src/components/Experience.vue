<template>
  <section class="container experience" id="experience">
    <h2>Skills</h2>
    <div class="experience-grid-container">
      <div class="category-container br-2">
        <h3>Languages</h3>
        <ul class="category-list two-col-list">
          <li>JavaScript</li>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>Sass</li>
          <li>TypeScript</li>
          <li>PHP</li>
          <li>Java</li>
          <li>C#</li>
        </ul>
      </div>
      <div class="category-container br-2">
        <h3>Framework/Library</h3>
        <ul class="category-list two-col-list">
          <li>GatsbyJS</li>
          <li>React</li>
          <li>Vue.js</li>
          <li>Android Studio</li>
          <li>Unity</li>
        </ul>
      </div>
      <div class="category-container br-2">
        <h3>Database</h3>
        <ul class="category-list">
          <li>GraphQL</li>
          <li>MySQL</li>
        </ul>
      </div>
      <div class="category-container br-2">
        <h3>Productivity</h3>
        <ul class="category-list">
          <li>Jira</li>
          <li>Asana</li>
        </ul>
      </div>
      <div class="category-container br-2">
        <h3>Software</h3>
        <ul class="category-list two-col-list">
          <li>Contentful</li>
          <li>Adobe Creative Suite</li>
          <li>Optimizely</li>
          <li>Figma</li>
          <li>Axure</li>
          <li>Sketch</li>
          <li>Adobe Experience Manager (AEM)</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.experience {
  margin: 2rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.experience-grid-container {
  gap: 1rem;
  margin-top: 2rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  @media screen and (min-width: 1110px) {
    align-items: stretch;
  }
}
.category-container {
  background: var(--cosmic-latte);
  padding: 2rem;
}
.category-list {
  list-style-type: none;
  padding: 0;
}
.two-col-list {
  columns: 2;
  -webkit-columns: 2;
  -moz-columns: 2;
  column-gap: 2rem;
  column-rule: 1px solid var(--carolina-blue);
}
</style>
