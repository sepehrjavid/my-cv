<template>
  <div class="experience-section">
    <div class="experience-card" v-for="experience in experiences" :key="experience.id">
      <div class="experience-header">
        <h3 class="job-title">{{ experience.title }}</h3>
        <p class="company-location">
          <span class="company">
            <i class="fas fa-building"></i> {{ experience.company }}
          </span> - 
          <span class="location">
            <i class="fas fa-map-marker-alt"></i> {{ experience.location }}
          </span>
        </p>
        <p class="dates"><i class="fas fa-calendar-alt"></i> {{ experience.date }}</p>
      </div>
      <ul class="experience-details">
        <li v-for="(detail, index) in experience.details" :key="index">
          <i class="fas fa-check-circle detail"></i> {{ detail }}
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
          title: 'Security and Infrastructure Engineer',
          company: 'Focalpay',
          location: 'Stockholm, Sweden',
          date: 'October 2023 - Present',
          details: [
            'Proposed and deployed a Canary deployment for enhanced progressive delivery.',
            'Introduced and deployed GCP Cloud Armor and API Gateway for improved traffic control and flexibility.',
            'Reduced GCP costs by 15.1% by eliminating redundant resources and optimizing resource types for cost efficiency.',
            'Added observability to the cluster using Grafana stack, identifying slow APIs and improving performance.',
            'Deploying and supporting a company\'s cloud solution using GKE, Bigquery, Kafka, Dataflow, and Cloud Function.'
          ]
        },
        {
          title: 'Cloud Networking Research Intern',
          company: 'Ericsson',
          location: 'Jorvas, Finland',
          date: 'July 2023 - Sep 2023',
          details: [
            'Engineered Sepittov2, an advanced congestion mitigation protocol improving SRv6 network latency by 64% which supports various congestion mitigation strategies based on packet QoS class.',
            'Designed an efficient latency observability for K8s cluster which utilized the user packets to piggyback telemetry data and reduce overhead telemetry traffic in the network.'
          ]
        },
        {
          title: 'Thesis Worker',
          company: 'Ericsson',
          location: 'Jorvas, Finland',
          date: 'Dec 2022 - Jun 2023',
          details: [
            'Obtained deep knowledge of eBPF programming and Linux network stack including Qdisc, XDP, Kprobes, and iptables.',
            'Conducted in-depth research on networking in the Linux kernel, eBPF programming, congestion control mechanisms, and packet manipulation.',
            'Engineered a sophisticated eBPF congestion control protocol (called Sepittov1) using packet manipulation and graph theory, improving network latency in an SRv6 network.'
          ]
        },
        {
          title: 'Research Intern',
          company: 'Ericsson',
          location: 'Jorvas, Finland',
          date: 'May 2022 - Aug 2023',
          details: [
            'Automated the installation of new Network Service Mesh (NSM) versions on Kubernetes using Ansible with different CNIs, leading to in-depth research on NSM functionality.',
            'Examined traffic shaping in Kubernetes with CNIs such as Calico and Cilium, performing in-depth research on each, leading to a paper submission.',
            'Performed deep research on SRv6 in Kubernetes CNIs and Linux kernel.'
          ]
        },
        {
          title: 'Django Developer',
          company: 'Timnak Travel Agency',
          location: 'Shiraz, Iran',
          date: 'Sep 2019 - Sep 2021',
          details: [
            'Iranjourney project management with agile methods and back-end development using Django REST framework, Django Channels, Redis, and PostgreSQL.',
            'Software testing using Django automated test tools as well as pytest',
            'Local Linux demo server and production server setup using Docker, Nginx, and Bind9.'
          ]
        },
        {
          title: 'Java Developer Intern',
          company: 'Rayanova',
          location: 'Shiraz, Iran',
          date: 'Mar 2019 - Jul 2019',
          details: [
            'Laboratory software development utilizing Java, JUnit test framework and Maven.',
            'Middle-ware development for insurance company API communications (SOAP) using Java.'
          ]
        },
        {
          title: 'Network Design Engineer Intern',
          company: 'Shiraz Central Post Office',
          location: 'Shiraz, Iran',
          date: 'Jul 2015 - Sep 2015',
          details: [
            'ARP spoofing with Cain & Abel and packet sniffing with Wireshark in the VOIP system for pen-testing.',
            'Participated in Cisco core switch upgrade on the network, and network troubleshooting.'
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

.experience-details {
  margin-top: 10px;
}

.experience-details li {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  font-size: 1em;
}

/* .detail {
  margin-right: 10px;
  color: #00acc1;
} */

svg {
  margin-right: 5px;
  color: #00acc1;
}
</style>
