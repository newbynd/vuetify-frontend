<template>
  <v-app>
    <head>
      <link href="https://use.fontawesome.com/releases/v5.0.13/css/all.css" rel="stylesheet">
    </head>
    <v-navigation-drawer
      v-model="drawer"
      clipped="true"
      floating="true"
      app
      dark
    >
      <v-list
          dense
          nav
          class="py-0"
        >
          <v-list-item two-line class="px-0">
            <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Néstor</v-list-item-title>
              <v-list-item-subtitle>Romero</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-divider></v-divider>

          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
    </v-navigation-drawer>

    <v-app-bar
      color="teal darken-1"
      dense
      dark 
      class="d-lg-none"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Néstor Romero Díaz</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>fab fa-linkedin</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>fab fa-github</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>fas fa-envelope</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <v-content class="grey darken-1" style="padding: 0px, 0px, 0px, 256px;">
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
      
      items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
    }),
};
</script>
