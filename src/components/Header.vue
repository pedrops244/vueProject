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

    <v-menu>
      <template #activator="{ props }">
        <v-btn icon class="mr-2" v-bind="props">
          <v-badge dot color="info">
            <v-icon icon="mdi-bell-outline"></v-icon>
          </v-badge>
        </v-btn>
      </template>
      <v-container
        style="
          width: 520px;
          top: 12px;
          left: 717px;
          max-height: 290px;
          max-width: 1319px;
          min-width: 48px;
          transform-origin: right top;
        "
      >
        <v-sheet overflow-hidden>
          <v-toolbar class="ps-4 pe-6" style="height: 48px"> View Read</v-toolbar>
          <v-divider aria-orientation="horizontal" role="separator"></v-divider>

          <v-responsive style="max-height: 340px; min-height: 204px; overflow-y: scroll">
            <v-list tabindex="0" role="listbox">
              <v-list-item class="pe-4 align-self-start" prepend-icon="mdi-cog">
                <v-list-item-title class="text-wrap text-h6">Updated Documentation Settings</v-list-item-title>
                <div class="text-caption mb-1 font-weight-bold text-medium-emphasis">Friday, August 25, 2023</div>
                <div class="text-medium-emphasis text-caption">
                  <p>
                    We’ve recently added some enhancements to the documentation’s settings drawer, including a new
                    Developer Mode that let’s you experiment with our upcoming GitHub integration.
                  </p>
                  <p>All sponsor <strong>$1</strong> or greater get to enjoy an Ad Free documentation experience.</p>
                </div>
              </v-list-item>
              <v-divider aria-orientation="horizontal" role="separator"></v-divider>
            </v-list>
            <v-list tabindex="0" role="listbox">
              <v-list-item class="pe-4 align-self-start" prepend-icon="mdi-star-box">
                <v-list-item-title class="text-wrap text-h6">Customized SLA from Vuetify </v-list-item-title>
                <div class="text-caption mb-1 font-weight-bold text-medium-emphasis">Wednesday, July 19, 2023</div>
                <div class="text-medium-emphasis text-caption">
                  <p>
                    Elevate your development team’s capabilities with a personalized support plan that provides direct
                    access to the <strong>Vuetify Core Development team</strong>. Get your questions answered by the
                    experts and receive invaluable guidance for your projects.
                  </p>
                </div>
              </v-list-item>
              <v-divider aria-orientation="horizontal" role="separator"></v-divider>
            </v-list>
            <v-list tabindex="0" role="listbox">
              <v-list-item class="pe-4 align-self-start" prepend-icon="mdi-controller">
                <v-list-item-title class="text-wrap text-h6">Unleash Your Vuetify Creativity!</v-list-item-title>
                <div class="text-caption mb-1 font-weight-bold text-medium-emphasis">Tuesday, May 16, 2023</div>
                <div class="text-medium-emphasis text-caption">
                  <p>
                    Dive into Vuetify Play today and bring your Vuetify projects to life with an immersive playground
                    experience. Unleash your creativity and explore the limitless possibilities of Vuetify!
                  </p>
                </div>
              </v-list-item>
              <v-divider aria-orientation="horizontal" role="separator"></v-divider>
            </v-list>
          </v-responsive>
        </v-sheet>
      </v-container>
    </v-menu>

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
