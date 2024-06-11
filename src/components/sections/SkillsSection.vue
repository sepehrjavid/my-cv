<template>
  <section class="skills">
    <h2>Skills</h2>
    <div class="skill-category" v-for="(category, index) in skillCategories" :key="index">
      <div class="category-header" @click="toggleCategory(index)">
        <i :class="category.icon"></i>
        <span>{{ category.name }}</span>
        <i :class="['fas', 'fa-chevron-down', { 'open': category.open }]"></i>
      </div>
      <ul v-show="category.open" class="skill-list">
        <li v-for="(item, i) in category.skills" :key="i">
          <div v-if="item.subSkills" @click="toggleSubCategory(category, i)" class="subcategory-header">
            {{ item.name }}
            <i :class="['fas', 'fa-chevron-down', { 'open': item.open }]"></i>
          </div>
          <ul v-show="item.open" v-if="item.subSkills" class="sub-skill-list">
            <li v-for="(subSkill, j) in item.subSkills" :key="j">
              {{ subSkill }}
            </li>
          </ul>
          <p v-else>{{ item }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SkillsSection',
  data() {
    return {
      skillCategories: [
        {
          name: 'Programming Languages',
          icon: 'fas fa-code',
          open: false,
          skills: ['JavaScript', 'Python', 'Java', 'C++']
        },
        {
          name: 'Frameworks & Libraries',
          icon: 'fas fa-cubes',
          open: false,
          skills: ['Vue.js', 'React', 'Node.js', 'Spring Boot']
        },
        {
          name: 'Tools & Platforms',
          icon: 'fas fa-tools',
          open: false,
          skills: [
            'Git',
            'Docker',
            'Kubernetes',
            {
              name: 'AWS',
              open: false,
              subSkills: ['EC2', 'S3', 'Lambda', 'RDS']
            }
          ]
        },
        {
          name: 'Databases',
          icon: 'fas fa-database',
          open: false,
          skills: ['MySQL', 'PostgreSQL', 'MongoDB']
        },
        {
          name: 'Soft Skills',
          icon: 'fas fa-user-friends',
          open: false,
          skills: ['Teamwork', 'Communication', 'Problem-solving']
        }
      ]
    };
  },
  methods: {
    toggleCategory(index) {
      this.skillCategories.forEach((category, i) => {
        category.open = i === index ? !category.open : false;
      });
    },
    toggleSubCategory(category, index) {
      category.skills.forEach((skill, i) => {
        if (skill.subSkills) {
          skill.open = i === index ? !skill.open : false;
        }
      });
    }
  }
};
</script>

<style scoped>
@import '~@fortawesome/fontawesome-free/css/all.css';

.skills {
  padding: 20px;
  background: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
  font-size: 2em;
}

.skill-category {
  margin-bottom: 10px;
  text-align: left;
}

.category-header, .subcategory-header {
  background: #0073e6;
  color: #fff;
  padding: 10px 15px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  transition: background 0.3s;
}

.category-header:hover, .subcategory-header:hover {
  background: #005bb5;
}

.category-header i, .subcategory-header i {
  margin-left: 10px;
  transition: transform 0.3s;
}

.category-header i.open, .subcategory-header i.open {
  transform: rotate(180deg);
}

.skill-list, .sub-skill-list {
  list-style-type: none;
  margin: 10px 0 0 0;
  padding: 0;
}

.skill-list li, .sub-skill-list li {
  background: #fff;
  padding: 10px;
  margin: 5px 15px;
  border: 1px solid #e0e0e0;
  border-radius: 5px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.skill-list li:hover, .sub-skill-list li:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
</style>
