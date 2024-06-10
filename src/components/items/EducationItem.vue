<template>
  <section class="education-item">
      <h3 class="degree">{{ educationInfo.title }} | <span class="university">{{educationInfo.university}}</span></h3>
      <div class="details">
        <div class="date-location">
          <i class="fas fa-calendar-alt"></i> {{educationInfo.period}}
          <span class="location"><i class="fas fa-map-marker-alt"></i> {{educationInfo.location}}</span>
        </div>
        <ul class="descriptions">
          <li v-for="point in educationInfo.points" :key="point.id">
            <p>{{ point.description }}</p>
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
