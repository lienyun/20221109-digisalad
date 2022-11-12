<template>
  <SideBar v-if="menu" @noSidebar="getCancel"></SideBar>
  <Nav @openMenu="getMenu" v-if="!menu"></Nav>
  <FirstPart v-if="!menu"></FirstPart>
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
    Awards, Service, Boss, Experience, Project, Nav
  },
  data(){
    return{
      menu: false
    }
  },
  methods:{
    getMenu(){
      this.menu = true
    },
    getCancel(){
      this.menu = false
    }
  }
}
</script>

<style lang="scss" scoped>
html,
body {
  position: relative;
}
</style>
