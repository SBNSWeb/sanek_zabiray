<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
    
      <v-list>
        <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Name of league
          </v-list-item-title>
          
          <v-list-item-subtitle>
            Season num
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      <v-toolbar-title v-text="title" />
      <v-spacer />
      
    </v-app-bar>

    <v-main style="background-image: url('https://cdn.wallpapersafari.com/7/74/JFeEHc.jpg');background-size:cover;background-position:center center; background-attachment:fixed;">
        <nuxt />
    </v-main>
   <v-footer
    color=""
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class=" py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          //icon: '/logo-delta.png',
          icon: 'mdi-apps',
          title: 'Главная',
          to: '/'
        },
        {
          icon: 'mdi-apps',
          title: 'Команды',
          to: '/inspire'
        },
        {
          icon:'mdi-apps',
          title:'Настройки',
          to:'/settings'
        },
        {
          icon:'mdi-apps',
          title:'Войти',
          to:'/auth'
        },
        {
          icon:'mdi-apps',
<<<<<<< HEAD
          title:'Cоздать команду',
=======
          title:'Create team',
>>>>>>> 6866de6fb0c3e3f35a4105791f18b8e6fdd2034b
          to:'/create'
        }
      ],
      links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Name of league'
    }
  },

}
</script>

<style>

</style>