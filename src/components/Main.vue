<template>
  <v-container>
    <v-layout row>
      <v-spacer />
      <v-flex>
        <v-layout column>
          <v-flex v-for="site in sites" :key="site">
            <v-card>
              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">{{site.name}}</h3>
                  <div>{{site.description}}</div>
                </div>
              </v-card-title>
              <v-card-actions>
                <v-btn flat :color="site.color" :href="website(site.link)">Visit</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-spacer />
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    sites: [
      {
        name: "School Planner",
        description: "A weekly planner for CC",
        color: "orange",
        link: "School_Planner"
      },
      {
        name: "Multiplication tables",
        description: "A game where you can review mulitplication facts",
        color: "blue",
        link: "MultiplicationTables"
      },
      {
        name: "Latin Vocabulary Review",
        description:
          "A game that asks which weeks you want to review then creates random questions with multiple choice answers",
        color: "purple",
        link: "LatinVocabReview"
      },
      {
        name: "Latin Charts",
        description:
          "A app where you fill in the other side of a chart with latin or english words",
        color: "dark-blue",
        link: "LatinCharts"
      },
      {
        name: "Take Over the World Game (By Rcbcodes)",
        description:
          "Take Over the World is a clicker game created by Rcbcodes WARNING: It is hard to stop playing",
        color: "red",
        link: "TakeOverTheWorldGame"
      },
      {
        name: "Latin Board",
        description:
          "Latin Board generates a 6x6 grid of latin vocabulary which you can use to review vocabulary",
        color: "deep-purple",
        link: "LatinBoard"
      }
    ]
  }),
  methods: {
    website(value) {
      return "/" + value;
    }
  }
};
</script>

<style>
</style>
