<template functional>
  <v-tooltip bottom>
    <template v-slot:activator="{ on, attrs }">
      <v-img v-bind="attrs" v-on="on" src="/homepage/logo.png" width="70vw"/>
    </template>

    <span>Designed by renata.s / Freepik</span>
  </v-tooltip>
</template>
