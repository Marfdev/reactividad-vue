<template>
  <form @submit.prevent="submitForm">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" v-model="refFormData.nombre" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" v-model="refFormData.email" required>
    
    <label for="contraseña">Contraseña:</label>
    <input type="password" id="contraseña" v-model="refFormData.contraseña" required>
    
    <button type="submit">Enviar</button>
  </form>
</template>

<script setup>
import { ref } from 'vue';

const initialFormData = {
  nombre: '',
  email: '',
  contraseña: ''
};

const refFormData = ref({
  ...initialFormData
});

const submitForm = () => {
  // Aquí puedes acceder a los valores del formulario a través de refFormData.value.<atributo> ( esto ultimo no es necesario con reactive() )
  
  alert(`Usuario ${refFormData.value.nombre} registrado correctamente`)

  // Limpiar el formulario con reemplazo de objeto ( esto no es posible con reactive() se tendria que hacer de otro modo)
  refFormData.value = { ...initialFormData };
};


</script>
