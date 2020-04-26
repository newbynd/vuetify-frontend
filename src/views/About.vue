<template>
  <v-container fluid> <!-- fluid para ocupar todo el espacio horizontal -->
    <v-row>
      <v-col cols="12">
        <v-row
          align="center"
          justify="center"
          class="amber lighten-4"
          style="height: 1000px;"
        >
          <v-card
            v-for="n in 3"
            :key="n"
            class="ma-3 pa-6"
            outlined
            tile
          >
            Column
          </v-card>
        </v-row>
      </v-col>    
    </v-row>
    
    <v-row>
        <v-col class="info" justify="center" align="center" cols="12">
          <v-btn class="primary mr-5" rounded="true">Accept</v-btn>
          <v-btn class="secondary" rounded="true">Cancel</v-btn>
        </v-col>
      </v-row>
  </v-container>
</template>
