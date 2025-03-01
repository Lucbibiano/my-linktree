<template>
    <div v-if="isOpen" class="fixed inset-0 flex items-center justify-center bg-black/50 backdrop-blur-md">
      <div class="bg-white rounded-2xl p-6 shadow-xl max-w-md w-full">
        <div class="flex justify-between items-center mb-4">
          <h2 class="text-lg font-semibold text-gray-800">Minhas Tecnologias</h2>
          <button @click="closeModal" class="text-gray-500 hover:text-gray-700 text-2xl">&times;</button>
        </div>
  
        <ul class="grid grid-cols-2 gap-4">
          <li v-for="(tech, index) in technologies" :key="index" class="flex items-center space-x-2">
            <img :src="tech.icon" :alt="tech.name" class="h-8 w-8">
            <span class="text-gray-700">{{ tech.name }}</span>
          </li>
        </ul>
  
        <button @click="closeModal" class="mt-4 w-full bg-blue-500 text-white py-2 rounded-lg hover:bg-blue-600">
          Fechar
        </button>
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from "vue";
  
  defineProps({
    isOpen: Boolean,
    closeModal: Function,
  });
  
  const technologies = [
  { name: "Vue.js", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" },
  { name: "Nuxt.js", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg" },
  { name: "JavaScript", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" },
  { name: "TypeScript", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" },
  { name: "Node.js", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" },
  { name: "Tailwind CSS", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" },
  { name: "Angular", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/angularjs/angularjs-original.svg" },
  { name: "React", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" },
  { name: "PostgreSQL", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" },
  { name: "MongoDB", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" },
  { name: "Java", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" },
  { name: "Kibana", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/elasticsearch/elasticsearch-original.svg" },
  { name: "Jenkins", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jenkins/jenkins-original.svg" },
  { name: "AWS", icon: "https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" },
  { name: "NestJS", icon: "https://upload.wikimedia.org/wikipedia/commons/a/a8/NestJS.svg" },
  { name: "RabbitMQ", icon: "https://upload.wikimedia.org/wikipedia/commons/7/71/RabbitMQ_logo.svg" },
  { name: "Azure DevOps", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg" },
  { name: "CI/CD", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gitlab/gitlab-original.svg" },
  { name: "SonarQube", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sonarqube/sonarqube-original.svg" },
  { name: "GitLab", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gitlab/gitlab-original.svg" },
  { name: "Docker", icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" }
];

  </script>
  