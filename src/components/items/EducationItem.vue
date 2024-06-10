<template>
  <section class="school">
    <h3><i class="fas fa-graduation-cap"></i> {{ educationInfo.degree }}</h3>
    <p class="institution"><i class="fas fa-university"></i> {{ educationInfo.institution }} - <span class="date"><i class="fas fa-calendar-alt"></i> {{ educationInfo.date }}</span></p>
    <p class="details">{{ educationInfo.details }}</p>
  </section>
</template>

<script>
export default {
  name: 'EducationItem',
  props: {
  educationInfo: {
   type: Object
  }
}
}
</script>

<style scoped>

.school {
  margin-bottom: 20px;
  padding: 20px;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  background: #fff;
  transition: transform 0.3s, box-shadow 0.3s;
}

.school:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.school h3 {
  margin: 0 0 10px;
  color: #0073e6;
  font-size: 1.5em;
}

.institution {
  font-weight: bold;
  color: #555;
  margin: 10px 0;
}

.date {
  font-style: italic;
  color: #999;
}

.details {
  color: #333;
}
</style>
