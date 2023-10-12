<template>
  <v-navigation-drawer v-model="isDrawerOpen">
    <v-list>
      <v-list-subheader>Menu</v-list-subheader>
      <v-list-item prepend-icon="mdi-home">Home</v-list-item>
      <v-list-item prepend-icon="mdi-account">Users</v-list-item>

      <v-list-group value="Clients">
        <template #activator="{ props }">
          <v-list-item v-bind="props" prepend-icon="mdi-account-circle" title="Clients"> </v-list-item>
        </template>
        <v-list-item prepend-icon="mdi-currency-usd">Sales</v-list-item>
        <v-list-item prepend-icon="mdi-chart-line">Report</v-list-item>
      </v-list-group>
    </v-list>
  </v-navigation-drawer>

  <v-app-bar flat class="border-b">
    <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>
    <v-app-bar-title>My APP</v-app-bar-title>

    <Notification />
    <Profile />
  </v-app-bar>
</template>
<script setup>
import { ref } from 'vue';
import Notification from '@/components/Notification.vue';
import Profile from '@/components/Profile.vue';

const isDrawerOpen = ref(false);
</script>
