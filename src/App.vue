<template>
  <SideBar @noSidebar="getCancel" v-if="menu"></SideBar>

  <Nav @openMenu="getMenu" v-if="!menu"></Nav>
  <FirstPart v-if="!menu"></FirstPart>
    <div t v-if="!menu" class="line-white"></div>

  <About v-if="!menu"></About>
  <Awards v-if="!menu"></Awards>
  <Service v-if="!menu"></Service>
  <Boss v-if="!menu"></Boss>
  <Experience v-if="!menu"></Experience>
  <Project v-if="!menu"></Project>
</template>

<script>
import SideBar from './components/sideBar.vue'
import FirstPart from './components/FirstPart.vue'
import About from './components/About.vue'
import Awards from './components/Awards.vue'
import Service from './components/Service.vue'
import Boss from './components/Boss.vue'
import Experience from './components/Experience.vue'
import Project from './components/Project.vue'
import Nav from './components/Nav.vue'


export default {
  name: 'App',
  components: {
    SideBar,
    FirstPart, About,
    Awards, Service, Boss, Experience, Project, Nav,
  },
  data() {
    return {
      menu: false,

    }
  },
  mounted() {

  },
  methods: {
    getMenu() {
      this.menu = true
    },
    getCancel() {
      this.menu = false
    },

  }
}
</script>

<style lang="scss" scoped>
html,
body {
  position: relative;
  // min-width: 560px;
}



.line-white {
    position: absolute;
    top: 97vh;
    left: 50%;
    width: 1px;
    // height: 44px;
    background: white;
    animation: showLine infinite;
    animation-duration: 1s;
}

@keyframes showLine {
  0% {
    height: 0;
  }
  100% {
    height: 120px;
  }
}

</style>

