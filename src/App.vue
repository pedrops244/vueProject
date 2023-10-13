<template>
  <v-app>
    <Header />
    <v-main>
      <v-container>
        <h1 class="mb-6">Dashboard</h1>

        <TableUsers />
        <v-row>
          <Card />
          <Card />
          <Card />
          <Card />
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import Card from '@/components/Card.vue';
import Header from '@/components/Header.vue';
import TableUsers from '@/components/TableUsers.vue';
</script>
