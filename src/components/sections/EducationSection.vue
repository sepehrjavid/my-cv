<template>
  <section class="education-section">
    <h2 class="section-title">EDUCATION</h2>
    <EducationItem v-for="education in educations" :key="education.id" :educationInfo="education"/>
  </section>
</template>

<script>
import EducationItem from '../items/EducationItem.vue'

export default {
  data() {
    return {
      educations: [
        {
          id: 1,
          title: "SECCLO",
          university: "Test",
          period: "HI",
          location: "Stockholm",
          points: [
            {id: 1, description: "it was nice"},
            {id: 2, description: "it was nice 2"},
          ]
        },
        {
          id: 1,
          title: "SECCLO",
          university: "Test",
          period: "HI",
          location: "Stockholm",
          points: [
            {id: 1, description: "it was nice"},
            {id: 2, description: "it was nice 2"},
          ]
        }
      ]
    }
  },
  name: 'EducationSection',
  components: {
    EducationItem
  }
}
</script>

<style scoped>
.education-section {
  background-color: #f0f0f0; /* Light gray background */
  padding: 20px;
  border-radius: 8px;
}

.section-title {
  font-size: 24px;
  font-weight: bold;
  border-bottom: 2px solid #555; /* Gray underline */
  margin-bottom: 16px;
  padding-bottom: 4px;
}

.education-item {
  margin-bottom: 24px;
}

.degree {
  font-size: 20px;
  font-weight: bold;
  margin: 0;
}

.university {
  color: #888; /* Gray color for university name */
  font-weight: normal;
}

.details {
  margin-left: 24px; /* Indentation for details */
}

.date-location {
  font-size: 14px;
  color: #555; /* Dark gray for date and location */
  display: flex;
  align-items: left;
  gap: 12px; /* Space between date and location */
}

.date-location i {
  margin-right: 8px; /* Space between icon and text */
}

.location {
  color: #000; /* Black color for location */
}

.descriptions {
  margin-top: 8px;
  padding-left: 24px; /* Indentation for descriptions */
  list-style-type: none;
}

.descriptions li {
  font-size: 14px;
  color: #777; /* Medium gray for descriptions */
}
</style>
