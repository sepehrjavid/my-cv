<template>
  <section>
      <h3 class="title"><i class="fas fa-briefcase"></i> {{ experienceInfo.title }}</h3>
      <p class="company"><i class="fas fa-building"></i> {{ experienceInfo.company }} - <span class="location"><i class="fas fa-map-marker-alt"></i> {{ experienceInfo.location }}</span></p>
      <p class="date"><i class="fas fa-calendar-alt"></i> {{ experienceInfo.date }}</p>
      <ul>
        <li v-for="(detail, i) in experienceInfo.details" :key="i"><i class="fas fa-check-circle"></i> {{ detail }}</li>
      </ul>
  </section>
</template>
  
<script>
  export default {
    name: 'ExperienceItem',
    props: {
      experienceInfo: {
       type: Object
      }
    }
  }
</script>
  
<style scoped>
.company {
  font-weight: bold;
  color: #555;
  margin: 10px 0;
}

.location {
  font-style: italic;
  color: #999;
}

.date {
  color: #999;
  margin-bottom: 10px;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
  padding-left: 20px;
}

li {
  margin-bottom: 5px;
  color: #333;
}

li i {
  margin-right: 10px;
  color: #28a745;
}

.title {
  margin: 0 0 10px;
  color: #0073e6;
  font-size: 1.3em;
}
</style>
  