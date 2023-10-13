<template>
  <v-card-title>
    <v-btn variant="elevated" size="small" color="primary" @click="isDialogOpen = true">Adiconar usuário</v-btn>

    <v-dialog v-model="isDialogOpen" width="600px">
      <v-card>
        <v-card-title>Adicionar usuário</v-card-title>
        <v-card-text>
          <v-row>
            <v-col>
              <v-text-field label="Nome" variant="outlined" clearable></v-text-field>
            </v-col>
            <v-col>
              <v-text-field label="Email" variant="outlined" clearable></v-text-field>
            </v-col>
          </v-row>
          <v-select label="Cargo" variant="outlined" :items="['Admin', 'Gerente', 'Convidado']"></v-select>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn variant="elevated" color="success">Salvar</v-btn>
          <v-btn variant="tonal" color="error" @click="isDialogOpen = false">Cancelar</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-card-title>
</template>

<script setup>
import { ref } from 'vue';
const isDialogOpen = ref(false);
</script>
