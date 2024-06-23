<template>
    <section class="self-introduction">
      <div class="introduction-content">
        <p v-for="(paragraph, index) in paragraphs" :key="index">{{ paragraph }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SelfIntroductionSection',
    data() {
      return {
        // Example paragraphs; replace with your actual text
        paragraphs: [
          "Hello! My name is Sepehr Javid. I have always been fascinated by technology and its potential to solve real-world problems. Over the years, I've honed my skills in various programming languages and technologies, and I have a deep passion for learning and exploring new domains.",
          "Currently, I'm focused on cloud computing and edge technologies, working with AWS and Google Cloud to design scalable, secure, and efficient solutions. My experience spans across software development, network security, and systems engineering, allowing me to bring a holistic approach to any project I undertake.",
          "Looking forward, I'm excited to delve deeper into AI and machine learning, exploring how these technologies can transform industries and improve lives. I believe in the power of technology to drive change, and I'm eager to be a part of the journey towards a smarter, more connected world."
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  @import '~@fortawesome/fontawesome-free/css/all.css';
  
  /* General styles for the section */
  .self-introduction {
    padding: 20px;
    background-color: #1e1e1e; /* Dark background */
    border-radius: 10px;
    color: #ffffff; /* Light text */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5); /* Subtle shadow for depth */
    max-width: 800px; /* Optional: limit the width for better readability */
    margin: 20px auto; /* Center the section horizontally */
  }
  
  .introduction-content {
    text-align: left;
    line-height: 1.6; /* Improved readability */
    font-size: 1.1em;
  }
  
  .introduction-content p {
    margin-bottom: 15px; /* Space between paragraphs */
  }
  
  .introduction-content p:last-child {
    margin-bottom: 0; /* No margin for the last paragraph */
  }
  
  /* Responsive adjustments */
  @media (max-width: 768px) {
    .self-introduction {
      padding: 15px;
    }
  
    h2 {
      font-size: 1.5em;
    }
  
    .introduction-content {
      font-size: 1em;
    }
  }
  </style>
  