<template>
  <v-app dark>
    <v-main>
      <v-container>
        <v-row no-gutters>
          <v-col align="center">
            <logo/>
          </v-col>
        </v-row>

        <nuxt class="mb-10 mt-4"></nuxt>

        <navigation></navigation>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Navigation from "@/components/Navigation";

export default {
  components: { Logo, Navigation }
}
</script>
