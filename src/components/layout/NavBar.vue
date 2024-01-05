<template>
  <v-card>
    <v-layout>
      <v-navigation-drawer
        v-model="drawer"
        :rail="rail"
        permanent
        @mouseover="rail = false"
        @mouseleave="rail = true"
      >
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
          title="John Smith"
          nav
        >
        </v-list-item>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item
            prepend-icon="mdi-home-city"
            title="Home"
            value="home"
            to="/"
          >
          </v-list-item>

          <div class="menu-footer">
          
            <v-divider></v-divider>
  
            <v-list-item
              prepend-icon="mdi-help-circle-outline"
              title="About"
              value="about"
              to="/about"
            >
            </v-list-item>
          </div>
        </v-list>

        

      </v-navigation-drawer>
    </v-layout>
  </v-card>
</template>

<script setup>
import { ref } from 'vue'

  let drawer = ref(true)
  let rail = ref(true)
</script>

<style scoped>
  .menu-footer {
    margin-top: calc(100vh - 150px);
  }
</style>