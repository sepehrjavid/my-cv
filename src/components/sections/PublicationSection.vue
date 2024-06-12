<template>
  <section class="publications">
    <h2>Publications</h2>
    <div v-for="(publication, index) in publications" :key="index" class="publication">
      <h3>{{ publication.title }}</h3>
      <p class="conference">
        <i class="fas fa-university" style="margin-right: 4px;"></i>
        {{ publication.conference }} 
      </p>
      <p class="details">{{ publication.details }}</p>
      <a :href="publication.link" class="read-more" target="_blank">Read More</a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PublicationsSection',
  data() {
    return {
      publications: [
        {
          title: 'Benchmarking of Emulated Wireless Edge Cloud Connectivity',
          conference: 'IEEE WF-IoT 2022',
          details: 'With focus on edge-cloud connectivity for maritime environments.',
          link: 'https://ieeexplore.ieee.org/abstract/document/10152152'
        },
        {
          title: 'QoS-Aware Congestion Control using SRv6',
          conference: 'IEEE CSCN23',
          details: 'This paper introduces Sepittov2 protocol designed to mitigate network congestion using SRv6.',
          link: 'https://ieeexplore.ieee.org/abstract/document/10453127'
        },
        // Add more publications as needed
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

.publication {
  margin-bottom: 20px;
  text-align: left;
  background: #fff;
  padding: 15px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.publication:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.publication h3 {
  margin: 0 0 10px;
  color: #0073e6;
  transition: color 0.3s ease-in-out;
}

.publication:hover h3 {
  color: #005bb5;
}

.conference {
  margin: 0 0 5px;
  color: #555;
  display: flex;
  align-items: center;
}

.details {
  margin: 0 0 10px;
  color: #777;
}

.read-more {
  display: inline-block;
  margin-top: 10px;
  color: #0073e6;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease-in-out;
}

.read-more:hover {
  color: #005bb5;
}
</style>
