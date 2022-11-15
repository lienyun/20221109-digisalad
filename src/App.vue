<template>
  <SideBar @noSidebar="getCancel" v-show="menu"></SideBar>

  <Nav @openMenu="getMenu" v-show="!menu"></Nav>
  <FirstPart v-if="!menu"></FirstPart>
  <div v-show="!menu" class="line-white"></div>

  <About v-show="!menu"></About>
  <Awards v-show="!menu"></Awards>
  <Service v-show="!menu"></Service>
  <Boss v-show="!menu"></Boss>
  <Experience v-show="!menu"></Experience>
  <Project v-show="!menu"></Project>
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
  // position: relative;
  // min-width: 560px;
}

::v-deep * {
  outline: 1px solid black;
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

