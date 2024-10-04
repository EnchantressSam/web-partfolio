<template>
  <div id="app">
    <HeaderSection />
    <HeroSection />
    <AboutSection />
    <ProjectsSection />
    <ContactsSection />
    <FooterSection />
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue'
import HeroSection from './components/HeroSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactsSection from './components/ContactsSection.vue'
import FooterSection from './components/FooterSection.vue'
import AboutSection from './components/AboutSection.vue'

export default {
  name: 'App',
  components: {
    HeaderSection,
    HeroSection,
    AboutSection,
    ProjectsSection,
    ContactsSection,
    FooterSection
  }
}

</script>

<style>
/* Общие стили для тем */
.dark {
  background-color: #333;
  color: white;
}

html {
  scroll-behavior: smooth;
}

/* Дополнительные стили для компонентов */
#app {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}
 h2 {
    font-size: 2.5em;
    margin-bottom: 20px;
    color: #4C504F;
  }
</style>
