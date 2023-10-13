<template>
  <v-card flat class="border mb-4">
    <v-card-title> Últimos usuários </v-card-title>
    <v-table>
      <thead>
        <tr>
          <th>Nome</th>
          <th>E-mail</th>
          <th>Cargo</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <ContentTable />
        <ContentTable />
        <ContentTable />
      </tbody>
    </v-table>
  </v-card>
</template>

<script setup>
import ContentTable from '@/components/ContentTable.vue';
</script>
