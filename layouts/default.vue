<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title" />
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar color="primary" fixed app dark>
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>{{ `chevron_${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn icon active-class :to="'/'" color="grey lighten-3">
        <img src="/logo.png" alt="logo" />
      </v-btn>
      <v-toolbar-title to="/" v-text="title" />
      <v-spacer />
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="(item, i) in items" :key="i" :to="item.to" flat>
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-container grid-list-md>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="true" color="primary" dark app>
      <v-layout justify-center>
        <span>&copy; 2019 Yuhei Okazaki. All Rights Reserved.</span>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      items: [
        { icon: 'apps', title: 'Profile', to: '/profile' },
        { icon: 'apps', title: 'Works', to: '/works' },
        { icon: 'apps', title: 'Languages', to: '/languages' },
        { icon: 'apps', title: 'Skills', to: '/skills' },
        { icon: 'apps', title: 'Community', to: '/community' },
        { icon: 'apps', title: 'Contact', to: '/contact' }
      ],
      miniVariant: false,
      title: "yuuu's portfolio"
    }
  }
}
</script>
