<template>
    <ion-card>
      <ion-card-header>
        <ion-card-title>{{ nombre }}</ion-card-title>
      </ion-card-header>
      <ion-card-content>
        <p>{{ descripcion }}</p>
        <pre>{{ codigo }}</pre>
        <ion-text color="primary">
          <span v-if="estado">Activado</span>
          <span v-else>Desactivado</span>
        </ion-text>
      </ion-card-content>
    </ion-card>
  </template>
  
  <script>
  export default {
    props: {
      nombre: String,
      descripcion: String,
      codigo: String,
      estado: Boolean
    }
  };
  </script>
  
  <style scoped>
  ion-card {
    margin-bottom: 10px;
  }
  </style>