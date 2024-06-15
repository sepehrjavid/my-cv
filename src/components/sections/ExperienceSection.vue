<template>
  <div class="experience-section">
    <h2>Experience</h2>
    <div class="experience-card" v-for="experience in experiences" :key="experience.id">
      <div class="experience-header">
        <h3 class="job-title">{{ experience.title }}</h3>
        <p class="company-location">
          <span class="company">{{ experience.company }}</span> - <span class="location">{{ experience.location }}</span>
        </p>
        <p class="dates">{{ experience.dates }}</p>
      </div>
      <ul class="experience-details">
        <li v-for="(detail, index) in experience.details" :key="index">
          <i class="fas fa-check-circle"></i> {{ detail }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      experiences: [
        {
          id: 1,
          title: "Security and Cloud Engineer",
          company: "Focalpay",
          location: "Stockholm, Sweden",
          dates: "October 2023 - Present",
          details: [
            "Proposed and deployed a Canary deployment for enhanced progressive delivery.",
            "Introduced and deployed GCP Cloud Armor and API Gateway for improved traffic control and flexibility.",
            "Reduced GCP costs by 15.1% by eliminating redundant resources and optimizing resource types for cost efficiency.",
            "Added observability to the cluster using Grafana stack, identifying slow APIs and improving performance.",
            "Deploying and supporting a company's cloud solution using GKE, Bigquery, Kafka, Dataflow, and Cloud Function."
          ]
        },
        {
          id: 2,
          title: "Cloud Networking Research Intern",
          company: "Ericsson",
          location: "Jorvas, Finland",
          dates: "July 2023 - Sep 2023",
          details: [
            "Engineered Sepittov2, an advanced congestion mitigation protocol improving SRv6 network latency by 64% which supports various congestion mitigation strategies based on packet QoS class.",
            "Designed an efficient latency observability for K8s cluster which utilized the user packets to piggyback telemetry data and reduce overhead telemetry traffic in the network."
          ]
        },
        {
          id: 3,
          title: "Thesis Worker",
          company: "Ericsson",
          location: "Jorvas, Finland",
          dates: "January 2023 - June 2023",
          details: [
            // Add your details here
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
.experience-section {
  padding: 20px;
}

.experience-section h2 {
  font-size: 1.8em;
  margin-bottom: 20px;
  color: #00acc1;
}

.experience-card {
  background-color: #2b2b2b;
  color: #cfcfcf;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
  transition: transform 0.3s, box-shadow 0.3s;
}

.experience-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.7);
}

.experience-header {
  margin-bottom: 15px;
}

.job-title {
  margin: 0 0 5px 0;
  font-size: 1.5em;
  color: #00acc1;
}

.company-location {
  margin: 0;
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
  margin: 0;
  font-size: 0.9em;
  color: #aaaaaa;
}

.experience-details {
  margin-top: 10px;
}

.experience-details li {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  font-size: 1em;
}

.experience-details i {
  margin-right: 10px;
  color: #00acc1;
}
</style>
