<template>
    <form @submit.prevent="submitForm">
      <label for="nombre">Nombre:</label>
      <input type="text" id="nombre" v-model="reactiveFormData.nombre" required>
      
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="reactiveFormData.email" required>
      
      <label for="contraseña">Contraseña:</label>
      <input type="password" id="contraseña" v-model="reactiveFormData.contraseña" required>
      
      <button type="submit">Enviar</button>
    </form>
  </template>
  
  <script setup>
  import { reactive } from 'vue';
  
  const initialFormData = {
    nombre: '',
    email: '',
    contraseña: ''
  };
  
  const reactiveFormData = reactive({
    ...initialFormData
  });
  
  const submitForm = () => {
    // Al ser Reactive, no necesitamos llamar a .value para acceder a los valores del formulario
    
    alert(`Usuario ${reactiveFormData.nombre} registrado correctamente`)
  
    // Limpiar el formulario, esta manera es mas pesada, ya que no se puede reemplazar el objeto completo directamente como con ref()
    // en un caso mas complejo se tendria que tratar cada atributo por separado (o por lso tipos de datos) ya que no todos los campos serian strings
    Object.keys(reactiveFormData).forEach(key => {
        formData[key] = ''
    })
  };
  
  
  </script>
  