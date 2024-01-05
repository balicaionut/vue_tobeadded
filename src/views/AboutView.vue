<template>
  <div class="about-container">
    <h1>ToBeAdded</h1>

    <v-divider class="divider"></v-divider>

    <p>{{ description }}</p>
    <p class="version">Current Version: {{ version }}</p>

    <v-divider class="divider"></v-divider>

    <div>
      <p style="font-weight: bold; font-size: 1.2rem;">Change log:</p>
      <p style="font-weight: bold;">version 0.0.1</p>
      <ul class="change-list">
        <li>Added About page</li>
        <li>Added Home page</li>
        <li>Added NavBar</li>
        <li>Added Vuetify</li>
        <li>Added Vue Router</li>
        <li>Deleted initial template</li>
      </ul>
      <p style="font-weight: bold;">version 0.0.0</p>
      <ul class="change-list">
        <li>Add Vue 3 template and recommended IDE setup</li>
        <li>Initial commit</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const description = ref('This is an all-in-one modular application.');
const version = ref('0.0.1');
</script>

<style scoped>
.about-container {
  padding-left: 4rem;
  padding-top: 1rem;
}

p {
  margin-top: 1rem;
}

.change-list {
  list-style-type: disc;
  margin-left: 2rem;
}

.version {
  font-size: smaller;
  font-weight: bold;
  margin-bottom: 1rem;
}

.divider {
  opacity: 1 !important;
  border-color: #d8d8d8 !important;
}
</style>