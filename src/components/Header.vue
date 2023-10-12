<template>
  <v-app-bar flat class="border-b">
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-app-bar-title>Meu app</v-app-bar-title>

    <v-btn icon class="mr-2">
      <v-badge dot color="info">
        <v-icon icon="mdi-bell-outline"></v-icon>
      </v-badge>
    </v-btn>

    <v-avatar>
      <v-img
        cover
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT72Uz03ApvOW6KNnQNCTlahJaeRH1ZaHaT-B5FldV9_i4mCwYmjHLQdQBci1_r35ohEps&usqp=CAU"
      ></v-img>
    </v-avatar>
  </v-app-bar>
</template>

<script setup></script>
