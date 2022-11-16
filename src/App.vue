<template>
  <SideBar @noSidebar="getCancel" v-show="menu"></SideBar>

  <Nav @openMenu="getMenu" v-show="!menu"></Nav>
  <FirstPart v-if="!menu"></FirstPart>
  <div v-show="!menu" class="line-white"></div>
  <div  v-show="!menu" class="swipe"></div>
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
// ::v-deep * {
//   outline: 1px solid black;
// }

.line-white {
  position: absolute;
  top: 97vh;
  left: 50%;
  width: 1px;
  // height: 44px;
  background: white;
  animation: showLine infinite;
  animation-duration: 2s;
}

.swipe {
  position: absolute;
  background: white;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  // top: 70vh;
  left: 50%;
  transform: translate(-5px);
  animation: showLineRWD infinite;
  animation-duration: 2s;
  display: none;
}

@keyframes showLine {
  0% {
    height: 0;
  }

  70% {
    height: 120px;
    opacity: 1;
  }

  95% {
    opacity: 0;
  }
}

@keyframes showLineRWD {
  0% {
    top: 75vh;
  }
  80% {
    opacity: 1;
  }

  95% {
    top: 70vh;
    opacity: 0;
  }
}

@media(max-width:468px){
  .line-white{
    display: none;
  }
  .swipe{
    display: block;
  }
}
</style>

