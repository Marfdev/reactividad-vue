<template>
    <div>
      <form @submit.prevent>
        <label for="birthdate">Fecha de Nacimiento:</label>
        <input type="date" id="birthdate" v-model="birthdate" required>
        
      </form>
      
      <div>
        <p>{{ ageText }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  
  const birthdate = ref('');
  
  
  const ageText = computed(() => {
    const birthdateValue = new Date(birthdate.value);
    const today = new Date();
    const diff = today - birthdateValue;
    const ageInYears = Math.floor(diff / (1000 * 60 * 60 * 24 * 365));
      return `Tu edad es: ${ageInYears} años`;
  });
  </script>