<template>
  <!-- <SideBar></SideBar> -->
  <FirstPart></FirstPart>
  <About></About>
  <Awards></Awards>
  <Service></Service>
  <Boss></Boss>
  <Experience></Experience>
  <Project></Project>
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

export default {
  name: 'App',
  components: {
    SideBar,
    FirstPart,About,
    Awards, Service, Boss, Experience, Project
  }
}
</script>

<style lang="scss" scoped>
</style>
