<template>
  <v-app dark>
    <v-main>
      <v-container fill-height style="width: 50%">
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

<script>
export default {
  data () {
    return {
      items: [
        { title: 'Home', icon: 'mdi-view-dashboard' },
        { title: 'About', icon: 'mdi-forum' },
      ],
    }
  },
}
</script>
