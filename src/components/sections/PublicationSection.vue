<template>
  <section class="publications">
    <div v-for="(publication, index) in publications" :key="index" class="publication">
      <h3>
        {{ publication.title }}
      </h3>
      <p class="conference">
        <i class="fas fa-university icons"></i> {{ publication.conference }}
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
        }
        // Add more publications as needed
      ]
    };
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

/* General styles for the section */
.publications {
  padding: 20px;
  border-radius: 10px;
  color: #ffffff; /* White text */
}


.publication {
  margin-bottom: 20px;
  text-align: left;
  background: #333333; /* Darker background for publications */
  padding: 15px;
  border-radius: 10px;
  border: 1px solid #444444; /* Slightly lighter border */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5); /* Dark shadow */
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.publication:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.8); /* Stronger shadow on hover */
}

.publication h3 {
  margin: 0 0 10px;
  color: #00acc1; /* Accent color for title */
  display: flex;
  align-items: center;
}

.conference {
  margin: 0 0 5px;
  color: #bbbbbb; /* Lighter grey for details */
  display: flex;
  align-items: center;
}

.conference i {
  margin-right: 8px; /* Space between icon and text */
}

.details {
  margin: 0 0 10px;
  color: #dddddd; /* Slightly lighter grey for details text */
}

.read-more {
  display: inline-block;
  margin-top: 10px;
  color: #00acc1; /* Accent color for links */
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease-in-out;
}

.read-more:hover {
  color: #00acc3; /* Slightly lighter color on hover */
}

.icons {
  margin-right: 5px;
  color: #00acc1;
}

/* Adding some additional styling for smaller screens */
@media (max-width: 768px) {
  .publication {
    padding: 10px;
    font-size: 0.9em;
  }

  .publications {
    padding: 15px;
  }
}
</style>
