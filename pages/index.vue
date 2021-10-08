<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="logo py-4 d-flex justify-center">
      </v-card>
      <v-card>
        <v-img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Rick_and_Morty.svg/1200px-Rick_and_Morty.svg.png"
        max-height="225"
        contain
        alt="logo"
        class="mb-5"
        
      />
        <v-card-title class="headline">
          
          Bienvenido al visualizador de personajes de Rick and Morty
        </v-card-title>
        <v-card-text>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
                   
          <hr class="my-3">
          
          
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/personajes"
          >
            Personajes
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>
