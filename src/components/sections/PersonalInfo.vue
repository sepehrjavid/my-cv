<template>
  <section class="personal-info">
    <div class="title">
      <h2>Sepehr Javid</h2>
      <h3>Security and Cloud Engineer</h3>
    </div>
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
        { value: 'javid.sepehr77@gmail.com', icon: 'fas fa-envelope', link: 'mailto:javid.sepehr77@gmail.com' },
        { value: '+46 (0)73 506 9239', icon: 'fas fa-phone', link: 'tel:+46735069239' },
        { value: 'Stockholm, Sweden', icon: 'fas fa-map-marker-alt' },
        { value: 'linkedin.com/in/sepehr-javid', icon: 'fab fa-linkedin', link: 'https://linkedin.com/in/sepehr-javid' },
        { value: 'github.com/sepehrjavid', icon: 'fab fa-github', link: 'https://github.com/sepehrjavid' }
      ]
    };
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

.personal-info {
  padding: 15px;
  padding-top: 60px;
  margin-bottom: 10px;
  background-color: #1e1e1e; 
  color: #ffffff;
}

.title {
  text-align: center;
  margin-bottom: 15px;
  padding-top: 20px;
  color: #ffffff;
  font-size: 1.3em;
}

.info-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.info-item {
  background: #333333; /* Dark background for the info item */
  border: 1px solid #444444; /* Slightly lighter border */
  border-radius: 8px;
  margin: 10px;
  padding: 20px;
  display: flex;
  align-items: center;
  width: 250px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.info-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.icon-container {
  flex: 0 0 auto;
  margin-right: 15px;
}

.icon-container i {
  font-size: 2em;
  color: #1e88e5; /* Accent color for icons */
}

.text-container {
  text-align: left;
}

.text-container a, .text-container p {
  margin: 0;
  color: #1e88e5; /* Accent color for text */
  font-size: 1em;
  text-decoration: none;
}

.text-container a:hover {
  text-decoration: underline;
}
</style>
