<template>
    <section class="achievements">
      <h2>Achievements</h2>
      <div v-for="(achievement, index) in achievements" :key="index" class="achievement">
        <h3>{{ achievement.title }}</h3>
        <p class="details">{{ achievement.details }}</p>
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
            title: 'Achievement 1',
            details: 'Details of achievement 1'
          },
          {
            title: 'Achievement 2',
            details: 'Details of achievement 2'
          },
          // Add more achievements as needed
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  @import '~@fortawesome/fontawesome-free/css/all.css';
  
  h2 {
    text-align: center;
    margin-bottom: 20px;
    color: #333;
    font-size: 2em;
    position: relative;
    display: inline-block;
    padding-bottom: 10px;
  }
  
  .achievement {
    margin-bottom: 20px;
    text-align: left;
    background: #fff;
    padding: 15px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s;
  }
  
  .achievement:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .achievement h3 {
    margin: 0 0 10px;
    color: #0073e6;
    transition: color 0.3s;
  }
  
  .achievement:hover h3 {
    color: #005bb5;
  }
  
  .details {
    margin: 0 0 10px;
    color: #777;
  }
  </style>
  