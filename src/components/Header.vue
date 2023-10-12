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

    <v-btn icon class="mr-2">
      <v-badge dot color="info">
        <v-icon icon="mdi-bell-outline"></v-icon>
      </v-badge>
    </v-btn>

    <v-menu>
      <template #activator="{ props }">
        <v-avatar v-bind="props">
          <v-img
            cover
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT72Uz03ApvOW6KNnQNCTlahJaeRH1ZaHaT-B5FldV9_i4mCwYmjHLQdQBci1_r35ohEps&usqp=CAU"
          ></v-img>
        </v-avatar>
      </template>

      <v-card min-width="200px">
        <v-list density="compact" :lines="false" nav>
          <v-list-item to="#" prepend-icon="mdi-account-outline">
            <v-list-item-title>Profile</v-list-item-title>
          </v-list-item>

          <v-list-item to="#" prepend-icon="mdi-heart-outline">
            <v-list-item-title>Favorites</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-card>
    </v-menu>
  </v-app-bar>
</template>
<script setup>
import { ref } from 'vue';

const isDrawerOpen = ref(false);
</script>
