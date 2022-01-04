<template>
  <div id="app">
    <Navbar msg='Navigation' />
    <WelcomeSection />
    <AboutMe />
    <Projects />
    <Technologies />
    <Contact />
  </div>
</template>



<style lang='scss' >
  @import './Sass/App.scss';
</style>

<script>
import AboutMe from './components/AboutMe.vue'
import Contact from './components/Contact.vue'

import Navbar from './components/Navbar.vue'
import Projects from './components/Projects.vue'
import Technologies from './components/Technologies.vue'
import WelcomeSection from './components/WelcomeSection.vue'



export default {
  name: 'App',
  components: {
    Navbar,
    WelcomeSection,
    Projects,
    AboutMe,
    Technologies,
    Contact
  }
}
</script>

