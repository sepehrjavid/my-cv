<template>
  <section class="education-item">
      <h3 class="degree">{{ educationInfo.title }} | <span class="university">{{educationInfo.university}}</span></h3>
      <div class="details">
        <div class="date-location">
          <i class="fas fa-calendar-alt"></i>
          <span class="date">{{educationInfo.period}}</span>
          <span class="location"><i class="fas fa-map-marker-alt"></i> {{educationInfo.location}}</span>
        </div>
        <ul class="descriptions">
          <li v-for="point in educationInfo.points" :key="point.id">
            {{ point.description }}
          </li>
        </ul>
      </div>
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

.section-title {
  font-size: 24px;
  font-weight: bold;
  border-bottom: 2px solid #555; /* Gray underline */
  margin-bottom: 16px;
  padding-bottom: 4px;
  text-align: left; /* Align title to the left */
}

.education-item {
  margin-bottom: 24px;
  /* padding-left: 10%; */
}

.degree {
  font-size: 20px;
  font-weight: bold;
  margin: 0;
  text-align: left; /* Align title to the left */
}

.university {
  color: #888; /* Gray color for university name */
  font-weight: normal;
}

.details {
  text-align: left;
  margin-left: 15px; 
}

.date-location {
  margin-top: 5px;
  font-size: 14px;
  color: #555; /* Dark gray for date and location */
  display: flex;
  gap: 12px; /* Space between date and location */
  text-align: left; /* Align title to the left */
}

.date {
  display: flex;
  gap: 4px;
  text-align: left; /* Align date to the left */
}

.date-location i {
  margin-right: 8px;
}

.location {
  color: #000; /* Black color for location */
  text-align: left; /* Align title to the left */
}

.descriptions {
  margin-top: 8px;
  padding-left: 20px; /* Indentation for descriptions */
  list-style-type: disc; /* Show bullet points */
  list-style-position: inside; /* Bullets outside the text */
  text-align: left; /* Align location to the left */
}

.descriptions li {
  font-size: 14px;
  color: #777; /* Medium gray for descriptions */
}
</style>
