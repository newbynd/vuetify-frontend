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
      expand-on-hover="true"
    >
        <div>
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
          <v-divider></v-divider>
        </v-list>
        </div>

  
        <div>
          <v-list dense nav class="py-0" shaped>
          <v-list-item
            v-for="network in networks"
            :key="network.title"
            link
            class="my-2"
          >
            <v-list-item-icon>
              <v-icon>{{ network.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ network.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        </div>       

    </v-navigation-drawer>

    <v-app-bar
      color="teal darken-1"
      dark 
      class="d-lg-none"
      app
      inverted-scroll="false"
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

    <v-content class="hiii" style="padding: 0px, 0px, 0px, 256px;">
      <router-view/>
    </v-content>
  
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
      
      items: [
        { title: 'Extracto', icon: 'mdi-account-card-details', targett: "#fir" },
        { title: 'Experiencia', icon: 'mdi-tie', targett: "2" },
        { title: 'Formación', icon: 'mdi-school', targett: "3" },
        { title: 'Certificados', icon: 'mdi-certificate', targett: "4" },
      ],
      networks: [
        { title: 'Email', icon: 'mdi-email' },
        { title: 'Linkedin', icon: 'mdi-linkedin-box' },
        { title: 'GitHub', icon: 'mdi-github-circle' },
      ],
    }),
};
</script>

<style>
  .hiii {
    background: #43cea2;  /* fallback for old browsers */
background: -webkit-linear-gradient(to left, #185a9d, #43cea2);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to left, #185a9d, #43cea2); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

  }
</style>