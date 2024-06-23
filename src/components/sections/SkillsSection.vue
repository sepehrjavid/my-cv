<template>
  <section class="skills">
    <h2>Skills</h2>
    <div class="skill-category" v-for="(category, index) in skillCategories" :key="index">
      <div class="category-header" @click="toggleCategory(index)">
        <i :class="category.icon"></i>
        <span>{{ category.name }}</span>
        <div :class="{ 'open': category.open }">
          <i class="fas fa-chevron-down"></i>
        </div>
      </div>
        <ul v-show="category.open" class="skill-list">
          <li v-for="(item, i) in category.skills" :key="i">
            <div v-if="item.subSkills" @click="toggleSubCategory(category, i)" class="subcategory-header">
              {{ item.name }}
              <div :class="{ 'open': item.open }">
                <i class="fas fa-chevron-down"></i>
              </div>
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
          skills: ['C/C++', 'Python', 'Java', 'Javascript', 'Bash']
        },
        {
          name: 'Web Dev Tools/Frameworks',
          icon: 'fab fa-js',
          open: false,
          skills: ['Nodejs', 'Django', 'ReactsJs', 'Vuejs', 'Flask', 'Git', 'Nginx']
        },
        {
          name: 'Cloud',
          icon: 'fas fa-cloud',
          open: false,
          skills: [
            'Ansible',
            'Docker',
            'Kubernetes',
            'Terraform',
            'gRPC',
            'MQTT',
            'Network Service Mesh',
            'OpenStack',
            'gitLab Devops',
            'Kafka',
            'Grafana',
            'Prometheus',
            {
              name: 'Kubernetes CNIs',
              open: false,
              subSkills: ['Calico', 'Cilium']
            },
            {
              name: 'Google Cloud Platform (GCP)',
              open: false,
              subSkills: ['GKE', 'ComputeEngine', 'Storage', 'Dataflow', 'Big-query', 'Loadbalancer', 'Cloud Function', 'Cloud Armor']
            },
            {
              name: 'Amazon Web Service (AWS)',
              open: false,
              subSkills: ['S3', 'Lambda', 'DynamoDB', 'Pubsub', 'EC2', 'ECS', 'EKS', 'Cloud Watch', 'RDS', 'IAM']
            }
          ]
        },
        {
          name: 'Databases/Caching',
          icon: 'fas fa-database',
          open: false,
          skills: ['PostgreSQL', 'MongoDB', 'SQLite', 'Redis', 'Vault']
        },
        {
          name: 'Security',
          icon: 'fas fa-lock',
          open: false,
          skills: ['Metasploit', 'Cain&Abel', 'BurpSuite', 'WireGuard', 'strongSwan', 'BeEF', 'EthicalHacking', 'Informationsecurity', 'Networksecurity', 'Trivy', 'ScoutSuite']
        },
        {
          name: 'Networking',
          icon: 'fas fa-network-wired',
          open: false,
          skills: ['CCNA R&S and security', 'Wireshark', 'HLS', 'Fastclick', 'DPDK', 'SRv6', 'eBPF programming', 'Linux kernel network stack']
        },
        {
          name: 'Operating Systems',
          icon: 'fas fa-desktop',
          open: false,
          skills: ['Kali Linux', 'Linux Server and Desktop', 'Windows Server', 'MacOS']
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
}

h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #ffffff;
  font-size: 2em;
}

.skill-category {
  margin-bottom: 10px;
}

.category-header, .subcategory-header {
  background: #2d2d2d;
  color: #ffffff;
  padding: 10px 15px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  transition: background 0.3s;
}

.category-header:hover, .subcategory-header:hover {
  background: #1e88e5;
}

.category-header div, .subcategory-header div {
  margin-left: 10px;
  transition: transform 0.4s;
}

.category-header div.open, .subcategory-header div.open {
  transform: rotate(180deg);
}

.skill-list, .sub-skill-list {
  list-style-type: none;
  margin: 10px 0 0 0;
  padding: 0;
}

.skill-list li, .sub-skill-list li {
  background: #424242;
  padding: 10px;
  margin: 5px 15px;
  border-radius: 5px;
  transition: transform 0.3s, box-shadow 0.3s;
  color: #ffffff;
}

.skill-list li:hover, .sub-skill-list li:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.4);
}

/* Animations */
.slide-fade-enter-active {
  transition: all 0.5s ease;
}

.slide-fade-enter {
  transform: translateY(-10px);
  opacity: 0;
}
</style>
