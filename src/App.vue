<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <EducationSection/>
  <ExperienceSection/>
</template>

<script>
import EducationSection from './components/sections/EducationSection.vue'
import ExperienceSection from './components/sections/ExperienceSection.vue'
import '@fortawesome/fontawesome-free/css/all.css';
import '@fortawesome/fontawesome-free/js/all.js';


export default {
  name: 'App',
  components: {
    EducationSection,
    ExperienceSection
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
