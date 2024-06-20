<template>
  <div class="dashboard">
    <!-- Sidebar Navigation -->
    <nav class="sidebar">
      <PersonalInfo/>
      <ul>
        <li :class="{ active: activeSection === 'Experience' }" @click="activeSection = 'Experience'">
          <i class="fas fa-briefcase icons"></i> Experience
        </li>
        <li :class="{ active: activeSection === 'Education' }" @click="activeSection = 'Education'">
          <i class="fas fa-graduation-cap icons"></i> Education
        </li>
        <li :class="{ active: activeSection === 'Skills' }" @click="activeSection = 'Skills'">
          <i class="fas fa-cogs icons"></i> Skills
        </li>
        <li :class="{ active: activeSection === 'Certificates' }" @click="activeSection = 'Certificates'">
          <i class="fas fa-cogs icons"></i> Certificates
        </li>
        <li :class="{ active: activeSection === 'Publications' }" @click="activeSection = 'Publications'">
          <i class="fas fa-book icons"></i> Publications
        </li>
        <!-- Add more sections as needed -->
      </ul>
    </nav>

    <!-- Main Content Area -->
    <main class="content">
      <section v-if="activeSection === 'Experience'">
        <ExperienceSection />
      </section>
      <section v-if="activeSection === 'Education'">
        <EducationSection />
      </section>
      <section v-if="activeSection === 'Skills'">
        <SkillsSection />
      </section>
      <section v-if="activeSection === 'Certificates'">
        <Certificates />
      </section>
      <section v-if="activeSection === 'Publications'">
        <PublicationSection />
      </section>
      <!-- Add more sections as needed -->
    </main>
  </div>
</template>

<script>
import ExperienceSection from './ExperienceSection.vue';
import EducationSection from './EducationSection.vue';
import SkillsSection from './SkillsSection.vue';
import PersonalInfo from './PersonalInfo.vue';
import Certificates from './Certificates.vue';
import PublicationSection from './PublicationSection.vue';
// import Skills from './Skills.vue';

export default {
  components: {
    ExperienceSection,
    EducationSection,
    SkillsSection,
    PersonalInfo,
    Certificates,
    PublicationSection
    // Add more sections as needed
  },
  data() {
    return {
      activeSection: 'Experience', // Default section
    };
  }
};
</script>

<style scoped>

.dashboard {
  display: flex;
  height: 100vh;
  width: 100vw;
  overflow: hidden; 
}

.sidebar {
  width: 25%; /* 20% width for the sidebar */
  height: 100%; 
  background-color: #1e1e1e;
  padding-top: 15px;
  padding: 25px;
  box-sizing: border-box;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.5);
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow-y: scroll;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
}

.sidebar li {
  padding: 15px 20px;
  margin-bottom: 10px;
  cursor: pointer;
  display: flex;
  align-items: center;
  font-size: 1.1em;
  color: #cfcfcf;
  border-radius: 8px;
  transition: background-color 0.3s;
}

.sidebar li:hover,
.sidebar li.active {
  background-color: #00acc1;
  color: #ffffff;
}

.icons {
  margin-right: 10px;
}

.content {
  width: 80%; /* 80% width for the content area */
  height: 100%; /* Full height for the content area */
  padding: 40px;
  box-sizing: border-box;
  overflow-y: auto; /* Enable vertical scrolling */
}

.content section {
  margin-bottom: 40px;
}

/* Style for the scrollbar in the content area */
.content::-webkit-scrollbar {
  width: 8px;
}

.content::-webkit-scrollbar-thumb {
  background-color: #00acc1;
  border-radius: 4px;
}

.content::-webkit-scrollbar-track {
  background-color: #2b2b2b;
}
</style>
