<template>
  <section class="achievements">
    <div v-for="(achievement, index) in achievements" :key="index" class="achievement">
      <h3> {{ achievement.title }}</h3>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AchievementsSection',
  data() {
    return {
      achievements: [
        {
          title: 'Junction 2021 Winner in Sustainable Data Infrastructure Challenge By Aiven'
        },
        {
          title: 'Erasmus Mundus Full Scholar among 542 applicants'
        }
        // Add more achievements as needed
      ]
    };
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

/* General styles for the section */
.icons {
  margin-right: 5px;
  color: #00acc1;
}

.achievement {
  margin-bottom: 20px;
  text-align: left;
  background: #333333; /* Darker background for achievements */
  padding: 15px;
  border-radius: 10px;
  border: 1px solid #444444; /* Slightly lighter border */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5); /* Dark shadow */
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.achievement:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.8); /* Stronger shadow on hover */
}

.achievement h3 {
  margin: 0 0 10px;
  color: #00acc1; /* Accent color for title */
  display: flex;
  align-items: center;
}

.achievement h3 i {
  margin-right: 10px; /* Space between icon and text */
  font-size: 1.2em; /* Slightly larger icon */
  color: #ffd700; /* Gold color for trophy icon */
}

.achievement:hover h3 {
  color: #00accf; /* Slightly lighter color on hover */
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .achievement {
    padding: 10px;
    font-size: 0.9em;
  }

  .achievements {
    padding: 15px;
  }
}
</style>
