<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(personaje, $index) in personajes"
          :key="$index"
          
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ personaje.id }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="personaje.nombre" />
          </v-list-item-content>
          <img :src="personaje.imagen " alt="imagen">
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      
    </v-app-bar>
    
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
       personajes: [
        {
        id: 1,
        nombre: 'Morty',
        imagen:
        'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
        'id': 2,
        'nombre': 'Rick',
        'imagen':
        'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
        'id': 3,
        'nombre': 'Summer',
        'imagen':
        'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
        'id': 4,
        'nombre': 'Beth',
        'imagen':
        'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
        'id': 5,
        'nombre': 'Jerry',
        'imagen':
        'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
        ]
        
    }
  }
//  data () {
//    return {
//      clipped: false,
//      drawer: false,
//      fixed: false,
//      items: [
//        {
//          icon: 'mdi-apps',
//          title: 'Welcome',
//          to: '/'
//        },
//        {
//          icon: 'mdi-chart-bubble',
//          title: 'Inspire',
//          to: '/inspire'
//        }
//      ],
//      miniVariant: false,
//      right: true,
//      rightDrawer: false,
//      title: 'Vuetify.js'
//    }
//  }
}
</script>
