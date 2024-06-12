<template>
    <section class="certificates">
      <h2>Certificates</h2>
      <div v-for="(certificate, index) in certificates" :key="index" class="certificate">
        <h3>{{ certificate.title }}</h3>
        <p class="issuer">{{ certificate.issuer }}</p>
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
            title: 'Certificate 1',
            issuer: 'Issuer 1',
            details: 'Details of certificate 1'
          },
          {
            title: 'Certificate 2',
            issuer: 'Issuer 2',
            details: 'Details of certificate 2'
          },
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
  
  .issuer {
    margin: 0 0 5px;
    color: #555;
  }
  
  .details {
    margin: 0 0 10px;
    color: #777;
  }
  </style>
  