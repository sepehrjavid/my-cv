<template>
  <section class="experience">
    <h2>Experience</h2>
    <div v-for="(job, index) in experiences" :key="index" class="job">
      <h3><i class="fas fa-briefcase"></i> {{ job.title }}</h3>
      <p class="company"><i class="fas fa-building"></i> {{ job.company }} - <span class="location"><i class="fas fa-map-marker-alt"></i> {{ job.location }}</span></p>
      <p class="date"><i class="fas fa-calendar-alt"></i> {{ job.date }}</p>
      <ul>
        <li v-for="(detail, i) in job.details" :key="i"><i class="fas fa-check-circle"></i> {{ detail }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ExperienceSection',
  data() {
    return {
      experiences: [
        {
          title: 'Security and Infrastructure Engineer',
          company: 'Focalpay',
          location: 'On-site',
          date: 'October 2023 - Present',
          details: [
            'Proposed and deployed a Canary deployment for enhanced progressive delivery.',
            'Introduced and deployed GCP Cloud Armor and API Gateway for improved traffic control and flexibility.',
            'Reduced GCP costs by 15.1% by eliminating redundant resources and optimizing resource types for cost efficiency.',
            'Added observability to the cluster using Grafana stack, identifying slow APIs and improving performance.',
            'Deploying and supporting a company’s cloud solution using GKE, Bigquery, Kafka, Dataflow, and Cloud Function.'
          ]
        },
        {
          title: 'Cloud Networking Research Intern',
          company: 'Ericsson',
          location: 'Hybrid',
          date: 'July 2023 - Sep 2023',
          details: [
            'Engineered Sepittov2, an advanced congestion mitigation protocol improving SRv6 network latency by 64% which supports various congestion mitigation strategies based on packet QoS class.',
            'Designed an efficient latency observability for K8s cluster which utilized the user packets to piggyback telemetry data and reduce overhead telemetry traffic in the network.'
          ]
        },
        {
          title: 'Thesis Worker',
          company: 'Ericsson',
          location: 'Hybrid',
          date: 'Dec 2022 - Jun 2023',
          details: [
            'Obtained deep knowledge of eBPF programming and Linux network stack including Qdisc, XDP, Kprobes, and iptables.',
            'Conducted in-depth research on networking in the Linux kernel, eBPF programming, congestion control mechanisms, and packet manipulation.',
            'Engineered a sophisticated eBPF congestion control protocol (called Sepittov1) using packet manipulation and graph theory, improving network latency in an SRv6 network compared.'
          ]
        },
        // Add other experiences similarly...
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

.job {
  margin-bottom: 20px;
  padding: 20px;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  background: #fff;
  transition: transform 0.3s, box-shadow 0.3s;
}

.job:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.job h3 {
  margin: 0 0 10px;
  color: #0073e6;
  font-size: 1.5em;
}

.company {
  font-weight: bold;
  color: #555;
  margin: 10px 0;
}

.location {
  font-style: italic;
  color: #999;
}

.date {
  color: #999;
  margin-bottom: 10px;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
  padding-left: 20px;
}

li {
  margin-bottom: 5px;
  color: #333;
}

li i {
  margin-right: 10px;
  color: #28a745;
}
</style>
