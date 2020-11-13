<template>
  <v-row>
    <v-col v-for="project in projects">
      <project :value="project"></project>
    </v-col>
  </v-row>
</template>


<script>
import Project from "@/components/Project"

export default {
  components: {Project},
  async asyncData({$axios}) {
    const projects = await $axios.$get('https://raw.githubusercontent.com/deen13/json-store/master/projects.json')

    return {projects}
  }
}
</script>
