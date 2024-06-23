<template>
    <MainDashboard/>
</template>

<script>
import MainDashboard from './components/sections/MainDashboard.vue'
import '@fortawesome/fontawesome-free/css/all.css';
import '@fortawesome/fontawesome-free/js/all.js';


export default {
  name: 'App',
  components: {
    MainDashboard
  }
}
</script>

<style>
body {
  padding: 0;
  margin: 0;
  /* display: flex; */
}


#app {
  background: #121212;
}
</style>
