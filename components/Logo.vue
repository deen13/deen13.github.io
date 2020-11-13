<template>
  <v-tooltip bottom>
    <template v-slot:activator="{ on, attrs }">
      <img v-bind="attrs" v-on="on" src="/logo.png" :width="$vuetify.breakpoint.mobile ? '80%' : '50%'"/>
    </template>

    <span>Designed by renata.s / Freepik</span>
  </v-tooltip>
</template>

