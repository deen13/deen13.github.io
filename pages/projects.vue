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
  components: { Project },
  data: () => ({
    projects: [
      {
        year: 2020,
        company: "Smartsquare GmbH",
        title: "Infrastruktur Monitoring",
        description: "In diesem Projekt wurde eine handgefertigte Monitoring-Lösung für einen Kunden implementiert, die neben den technischen Metriken auch historische fachliche Daten anaylisert.",
        tags: ['Kotlin', 'Nuxt.js', 'TimescaleDB']
      },
      {
        year: 2019,
        company: "Smartsquare GmbH",
        title: "Parkausverwaltung",
        description: "Im Zuge der Digitalisierung haben wir die Verwaltung von Parkhäusern in die Cloud gebracht. Neben der Analyse über die Auslastung und Wirtschaftlichkeit für die Betreiber können die Endkunden dort nun via Paypal, Apple Pay und Google Pay bezahlen.",
        tags: ['Vert.X', 'Kubernetes', 'MQTT']
      },
      {
        year: 2018,
        company: "Smartsquare GmbH",
        title: "Smartes Kickern",
        description: "Während eines Forschungsprojekt haben wir unseren Kicker mit Sensorik ausgestattet und ein Matchmaking System mit Elo-Ranking implementiert. Unser Fachartikel in dem Javamagazin hat dem Leser anhand des Beispiels einen kurzen Einsteig in das Thema Android Things geboten. ",
        tags: ['Android Things', 'Google Nearby', 'Reactive Programming']
      },
      {
        year: 2019,
        company: "Smartsquare GmbH",
        title: "S/PRI Portal",
        description: "Um den Glasfaser-Anschlusswechsel zu vereinfachen haben wir für einen Internetanbieter ein S/PRI Portal implementiert.",
        tags: ['Thymeleaf', 'Spring MVC', 'Spock']
      },
      {
        year: "2015 - 2018",
        company: "itelligence AG",
        title: "EDI Middleware",
        description: "Während meiner Ausbildung durfte ich an der Produktentwicklung einer Middleware zum Austausch von Gutschriften und Rechnungen zwischen Handelspartnern mitwirken.",
        tags: ['Java', 'OpenUI5']
      }
    ]
  })
}
</script>
