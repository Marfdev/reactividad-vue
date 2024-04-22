<template>
    <div>
      <h2>Contador: {{ count }}</h2>
      <button @click="increment">Añadir</button>
      <button @click="decrement">Restar</button>
      checkpoint: 20
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const count = ref(0);
  
  const increment = () => {
    count.value++;
  };
  
  const decrement = () => {
    count.value--;
  };
  
  watch(count, (newValue) => {
    if (newValue == 20) {
      alert('¡Has llegado al primer checkpoint!');
    }
  });
  </script>