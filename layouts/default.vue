<template>
  <v-app dark>
    <v-main>
      <v-container fill-height :style="$vuetify.breakpoint.mobile ? 'width: 90%' : 'width: 50%'">
        <v-row align="center" justify="center">
          <logo></logo>

          <nuxt class="mt-10"></nuxt>

          <v-btn v-if="$nuxt.$route.path === '/'" x-large dark nuxt to="/projects">
            Projekte
          </v-btn>
          <v-btn v-else x-large dark nuxt to="/">
            Home
          </v-btn>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
