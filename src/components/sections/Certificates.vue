<template>
    <section class="certificates">
      <h2>Certificates</h2>
      <div v-for="(certificate, index) in certificates" :key="index" class="certificate">
        <h3>{{ certificate.title }}</h3>
        <p class="issuer">
            <i class="fas fa-building"></i> 
            {{ certificate.issuer }}
        </p>
        <p class="issue-date">
            <i class="fas fa-calendar-alt"></i>
            {{ certificate.issueDate }}
        </p>
        <p class="details">{{ certificate.details }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'CertificatesSection',
    data() {
      return {
        certificates: [
          {
            title: 'AWS Cloud Technical Essentials',
            issuer: 'Amazon Web Service (AWS)',
            issueDate: 'January 2020',
            details: 'Hands on experience with many AWS services such as IAM, DynamoDB, EC2, Lambda, ECS, Cloudwatch, S3, RDS, etc.'
          },
          {
            title: 'Next-Gen Data Center Security Cloud Guard for Google Cloud',
            issuer: 'Google Cloud',
            issueDate: 'January 2020',
            details: 'Lab work experience with GloudGaurd.'
          },
          {
            title: "Hardening Default GKE Cluster Configurations",
            issueDate: 'January 2020',
            issuer: "Google Cloud",
            details: "Hands on practice with GKE and pod security conecrns such as pod escape and priviledge escalation."
          },
          {
            title: "Cloud Computing Basics (Cloud 101)",
            issueDate: 'January 2020',
            issuer: "LearnQuest",
            details: "Introduction to different cloud platforms, cloud deployment modules, and understanding manged services. "
          }
          // Add more certificates as needed
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
  
  .certificate {
    margin-bottom: 20px;
    text-align: left;
    background: #fff;
    padding: 15px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  }
  
  .certificate:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .certificate h3 {
    margin: 0 0 10px;
    color: #0073e6;
    transition: color 0.3s ease-in-out;
  }
  
  .certificate:hover h3 {
    color: #005bb5;
  }
  
  .issuer .issue-date {
    margin: 0 0 5px;
    color: #555;
  }
  
  .details {
    margin: 0 0 10px;
    color: #777;
  }
  </style>
  