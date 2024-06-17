<template>
  <section class="certificates">
    <div v-for="(certificate, index) in certificates" :key="index" class="certificate">
      <h3>{{ certificate.title }}</h3>
      <p class="issuer">
        <i class="fas fa-building icons"></i> {{ certificate.issuer }}
      </p>
      <p class="issue-date">
        <i class="fas fa-calendar-alt icons"></i> {{ certificate.issueDate }}
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
          issueDate: 'June 4, 2024',
          details: 'Hands on experience with many AWS services such as IAM, DynamoDB, EC2, Lambda, ECS, Cloudwatch, S3, RDS, etc.'
        },
        {
          title: 'Next-Gen Data Center Security Cloud Guard for Google Cloud',
          issuer: 'Google Cloud',
          issueDate: 'April 9, 2024',
          details: 'Lab work experience with GloudGaurd.'
        },
        {
          title: "Hardening Default GKE Cluster Configurations",
          issueDate: 'March 18, 2024',
          issuer: "Google Cloud",
          details: "Hands on practice with GKE and pod security conecrns such as pod escape and priviledge escalation."
        },
        {
          title: "Cloud Computing Basics (Cloud 101)",
          issueDate: 'March 18, 2024',
          issuer: "LearnQuest",
          details: "Introduction to different cloud platforms, cloud deployment modules, and understanding manged services."
        }
        // Add more certificates as needed
      ]
    };
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

/* General styles for the section */
/* .certificates {
  padding: 20px;
  background-color: #1e1e1e; 
  border-radius: 10px;
  color: #ffffff;
} */
.icons {
  margin-right: 5px;
  color: #00acc1;
}

.certificate {
  margin-bottom: 20px;
  text-align: left;
  background: #333333; /* Darker background for certificates */
  padding: 15px;
  border-radius: 10px;
  border: 1px solid #444444; /* Slightly lighter border */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5); /* Dark shadow */
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.certificate:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.8); /* Stronger shadow on hover */
}

.certificate h3 {
  margin-bottom: 20px;
  color: #00acc1;
  margin: 0 0 10px;
  display: flex;
  align-items: center;
}

.certificate h3 i {
  margin-right: 10px; /* Space between icon and text */
}

.issuer {
  font-weight: bold;
}

.issue-date {
  font-size: 0.9em;
}

.issuer, .issue-date, .details {
  margin: 0 0 5px;
  color: #bbbbbb; /* Lighter grey for details */
}

.issuer i, .issue-date i {
  margin-right: 10px; /* Space between icon and text */
}

/* Adding some additional styling for smaller screens */
@media (max-width: 768px) {
  .certificate {
    padding: 10px;
    font-size: 0.9em;
  }

  .info-container {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>
