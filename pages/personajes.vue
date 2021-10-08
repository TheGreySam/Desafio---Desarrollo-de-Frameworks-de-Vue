<template>
  <v-row>
    <v-col class="text-center">
      <v-img
        src="https://cdn11.bigcommerce.com/s-fg272t4iw0/images/stencil/1280x1280/products/7093/7346/C-17141__68476.1557818587.jpg?c=2"
        max-height="325"
        contain
        alt="logo"
        class="mb-5"
      />
      
      <h1>Lista de Rick and Morty</h1>
      <v-card v-for="(personaje, $index) in personajes"
          :key="$index"
          >
 
            <img :src="personaje.imagen" />
            <h1>{{personaje.nombre}}</h1>
          </v-card>
    </v-col>
  </v-row>
</template>

<script>


export default {
    data: () => ({
        personajes: [
        {
        id: 1,
        nombre: 'Morty',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
        id: 2,
        nombre: 'Rick',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
        id: 3,
        nombre: 'Summer',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
        id: 4,
        nombre: 'Beth',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
        id: 5,
        nombre: 'Jerry',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
        ]
    }),
//    computed: {
//        imgPersonaje() {
//            return `https://rickandmortyapi.com/api/character/avatar/5.jpeg`;
//              return this.$state.personajes.imagen;
//        }
//    }
}    
</script>
