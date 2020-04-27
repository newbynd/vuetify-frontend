<template>
  <v-container fluid class="fill-heigth px-0 py-0">

<!-- INTRO-->
      <div class="v-responsive v-image" style="height: 100vh;">
          <div class="v-image__image v-image__image--cover" style="background-image: url(&quot;https://material-portfolio-dark.vuetifyjs.com/img/hero.e530afc6.png&quot;); background-position: center center;"></div>
            <div class="v-responsive__content" style="width: 1922px;">
                <div class="row fill-height text-right pa-md-5 pa-3 mx-0 align-end justify-end">
                    <div class="mb-5 mr-5">
                        <div class="display-3 teal--text lighten-">Néstor Romero Díaz</div>
                        <h1 class="teal--text text--accent-3 display-4">DevOps Developer</h1>
                    </div>
                </div>
            </div>
      </div>

<!-- EXTRACTO-->
    <v-row>
        <v-col class="py-0 px-0" justify="center" align="center" cols="12" style="height: 100vh;">
            <v-card light max-width="500" class="mt-10 success" elevation="30" hover="true">
                <v-card-text>
                    hi
                </v-card-text>

            </v-card>
        </v-col>
    </v-row>

<!-- PARALLAX-->
    <v-row> 
        <v-col class="py-0" justify="center" align="center" cols="12">
            <v-parallax
            dark
            src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
            style="height: 50vh;"
            >
                <v-row
                align="center"
                justify="center"
                >
                    <v-col class="text-center" cols="12">
                        <h1 class="display-1 font-weight-thin mb-4">Vuetify.js</h1>
                        <h4 class="subheading">Build your application today!</h4>
                    </v-col>
                </v-row>
            </v-parallax>
        </v-col>
      </v-row>

<!-- TIMELINE-->
      <v-row>
        <v-col class="py-0 px-0" justify="center" align="center" cols="12" style="height: 100vh;">
            <div class="mx-10 my-10">
    <v-timeline style="max-width: 1000px;">
      <v-timeline-item
        v-for="n in 3"
        :key="n"
        icon-color= "teal accent-3"
        small="true"
        color="teal"
      >
        <span slot="opposite" class="white--text">2019</span>
        <v-card class="elevation-2">
          <v-card-title class="headline">Lorem ipsum</v-card-title>
          <v-card-text>
            Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
        </v-col>
    </v-row>

  </v-container> 
</template>

<script>
  export default {

  }
</script>

<style>

</style>