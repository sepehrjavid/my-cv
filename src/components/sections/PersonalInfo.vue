<template>
    <section class="personal-info">
      <h2>Personal Information</h2>
      <div class="info-container">
        <div class="info-item" v-for="(info, index) in personalInfo" :key="index">
          <div class="icon-container">
            <i :class="info.icon"></i>
          </div>
          <div class="text-container">
            <a v-if="info.link" :href="info.link" target="_blank" rel="noopener noreferrer">{{ info.value }}</a>
            <p v-else>{{ info.value }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'PersonalInfoSection',
    data() {
      return {
        personalInfo: [
          { value: 'Sepehr Javid', icon: 'fas fa-user' },
          { value: 'javid.sepehr77@gmail.com', icon: 'fas fa-envelope', link: 'mailto:john.doe@example.com' },
          { value: '+46 (0)73 506 9239', icon: 'fas fa-phone', link: 'tel:+46735069239' },
          { value: 'Stockholm, Sweden', icon: 'fas fa-map-marker-alt' },
          { value: 'linkedin.com/in/sepehr-javid', icon: 'fab fa-linkedin', link: 'https://linkedin.com/in/sepehr-javid' },
          { value: 'github.com/sepehravid', icon: 'fab fa-github', link: 'https://github.com/sepehrjavid' }
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
  }
  
  .info-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .info-item {
    background: #fff;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    margin: 10px;
    padding: 20px;
    display: flex;
    align-items: center;
    transition: transform 0.3s, box-shadow 0.3s;
    width: 250px;
  }
  
  .info-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }
  
  .icon-container {
    flex: 0 0 auto;
    margin-right: 15px;
  }
  
  .icon-container i {
    font-size: 2em;
    color: #0073e6;
  }
  
  .text-container {
    text-align: left;
  }
  
  .text-container a, .text-container p {
    margin: 0;
    color: #0073e6;
    font-size: 1em;
    text-decoration: none;
  }
  
  .text-container a:hover {
    text-decoration: underline;
  }
  </style>
  