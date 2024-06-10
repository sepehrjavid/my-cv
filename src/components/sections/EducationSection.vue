<template>
  <section class="education">
    <h2>Education</h2>
    <div v-for="(edu, index) in education" :key="index">
      <EducationItem :educationInfo="edu" :id="idenx"/>
    </div>
  </section>
</template>

<script>
import EducationItem from '../items/EducationItem.vue'

export default {
  name: 'EducationSection',
  components: {
    EducationItem
  },
  data() {
    return {
      education: [
        {
          degree: 'Master of Science in Security and Cloud Computing',
          institution: 'KTH and Aalto University',
          date: '2021 - 2023',
          details: 'Graduated with honor, CGPA: 4.59/5'
        },
        {
          degree: 'Bachelor of Science in Computer Science',
          institution: 'Shiraz University',
          date: '2017 - 2021',
          details: 'Graduated amongst top 10 out of 67 students, CGPA: 17.74/20'
        }
        // Add other education details similarly...
      ]
    };
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

.education {
  padding: 20px;
  background: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  max-width: 800px;
  margin: 0 auto;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
  font-size: 2em;
}

</style>
