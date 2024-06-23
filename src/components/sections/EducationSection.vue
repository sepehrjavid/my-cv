<template>
  <div class="education-section">
    <div class="education-card" v-for="education in educations" :key="education.id">
      <div class="education-header">
        <h3 class="job-title">{{ education.degree }}</h3>
        <p class="company-location">
          <span class="company">
            <i class="fas fa-graduation-cap"></i> {{ education.institution }}
          </span>
        </p>
        <p class="dates"><i class="fas fa-calendar-alt"></i> {{ education.date }}</p>
      </div>
      <p class="education-details">
        {{ education.details }}
      </p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'EducationSection',
  data() {
    return {
      educations: [
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
.education-section {
  padding: 20px;
}

.education-section h2 {
  font-size: 1.8em;
  margin-bottom: 20px;
  color: #00acc1;
}

.education-card {
  background-color: #2b2b2b;
  color: #cfcfcf;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
  transition: transform 0.3s, box-shadow 0.3s;
}

.education-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.7);
}

.education-header {
  margin-bottom: 15px;
}

.job-title {
  margin: 0;
  font-size: 1.5em;
  color: #00acc1;
}

.company-location {
  margin: 5px;
  font-size: 1em;
}

.company {
  font-weight: bold;
}

.location {
  font-style: italic;
  color: #aaaaaa;
}

.dates {
  margin: 5px;
  font-size: 0.9em;
  color: #aaaaaa;
}

.education-details {
  margin-top: 10px;
}

.education-details li {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  font-size: 1em;
}

svg {
  margin-right: 5px;
  color: #00acc1;
}
</style>
