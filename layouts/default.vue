<template>
  <v-app dark>
    <v-main>
      <v-container fill-height :style="$vuetify.breakpoint.mobile ? 'width: 90%' : 'width: 50%'">
        <v-row align="center" justify="center">
          <logo></logo>

          <nuxt class="mt-10"></nuxt>

          <navigation></navigation>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
