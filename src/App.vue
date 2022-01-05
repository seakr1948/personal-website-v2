<template>
  <div id="app" >
    
    <div :class="`overlay ${sidenav_open ? 'overlay-active' : ''}`"></div>
    <SideNav v-on:toggleState="changeState" :sidenav_open="sidenav_open" />
    <Navbar  v-on:toggleState="changeState" :sidenav_open="sidenav_open"/>
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
import SideNav from './components/SideNav.vue'
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
    Contact,
    SideNav
  },

  data() {
    return{
      sidenav_open: false
    }
  },

  methods: {
    changeState(val){
      this.sidenav_open = val;
    }
  }
}
</script>

