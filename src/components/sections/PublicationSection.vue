<template>
    <section class="publications">
      <h2>Publications</h2>
      <div v-for="(publication, index) in publications" :key="index" class="publication">
        <h3>{{ publication.title }}</h3>
        <p class="authors">{{ publication.authors }}</p>
        <p class="details">{{ publication.journal }}, {{ publication.year }}</p>
        <a :href="publication.link" target="_blank" class="publication-link">Read more</a>
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
            title: 'Title of Publication 1',
            authors: 'Author 1, Author 2',
            journal: 'Journal Name',
            year: 2020,
            link: 'https://example.com/publication1'
          },
          {
            title: 'Title of Publication 2',
            authors: 'Author 1, Author 2, Author 3',
            journal: 'Another Journal',
            year: 2021,
            link: 'https://example.com/publication2'
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
    transition: transform 0.3s, box-shadow 0.3s;
  }
  
  .publication:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .publication h3 {
    margin: 0 0 10px;
    color: #0073e6;
    transition: color 0.3s;
  }
  
  .publication:hover h3 {
    color: #005bb5;
  }
  
  .authors {
    margin: 0 0 5px;
    color: #555;
  }
  
  .details {
    margin: 0 0 10px;
    color: #777;
  }
  
  .publication-link {
    color: #0073e6;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .publication-link:hover {
    color: #005bb5;
  }
  </style>
  