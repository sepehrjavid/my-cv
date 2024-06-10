<template>
  <div class="cv">
    <PersonalInfo/>
    <EducationSection/>
    <ExperienceSection/>
    <SkillsSection/>
  </div>  
</template>

<script>
import EducationSection from './components/sections/EducationSection.vue'
import ExperienceSection from './components/sections/ExperienceSection.vue'
import PersonalInfo from './components/sections/PersonalInfo.vue'
import SkillsSection from './components/sections/SkillsSection.vue'
import '@fortawesome/fontawesome-free/css/all.css';
import '@fortawesome/fontawesome-free/js/all.js';


export default {
  name: 'App',
  components: {
    EducationSection,
    ExperienceSection,
    PersonalInfo,
    SkillsSection
  }
}
</script>

<style>

.cv {
  padding: 20px;
  background: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  max-width: 850px;
  margin: 0 auto;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
