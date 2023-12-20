<template>
  <v-card>
    <v-layout>
      <v-navigation-drawer
        v-model="drawer"
        :rail="rail"
        permanent
        @click="rail = false"
      >
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
          title="John Smith"
          nav
        >
          <template v-slot:append>
            <v-btn
              variant="text"
              icon="mdi-chevron-left"
              @click.stop="rail = !rail"
            ></v-btn>
          </template>
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
        </v-list>

        <div class="menu-footer">
          <v-divider></v-divider>

          <v-list density="compact" nav>
            <v-list-item
              prepend-icon="mdi-help-circle-outline"
              title="About"
              value="about"
              to="/about"
            >
            </v-list-item>
          </v-list>
        </div>

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
    position: absolute;
    bottom: 0;
    width: 100%;
  }
</style>