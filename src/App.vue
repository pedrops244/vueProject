<template>
  <v-app>
    <Header />
    <v-main>
      <v-container>
        <h1>Dashboard</h1>
        <Card />
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import Card from '@/components/Card.vue';
import Header from '@/components/Header.vue';
</script>
