<template>
  <section class="experience">
    <h2>Work Experience</h2>
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h3>{{ job.title }}</h3>
        <p>{{ job.company }} - {{ job.duration }}</p>
        <p>{{ job.description }}</p>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          id: 1,
          title: 'Software Engineer',
          company: 'Tech Corp',
          duration: 'Jan 2020 - Present',
          description: 'Developed awesome software.'
        },
        // Add more jobs here
      ]
    }
  }
}
</script>

<style scoped>
.experience {
  /* Add your styles here */
}
</style>
