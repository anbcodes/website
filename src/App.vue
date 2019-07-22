<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">Anbcodes</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon href="https://github.com/anbcodes">
        <img src="./assets/GitHub-Mark/PNG/GitHub-Mark-32px.png" />
      </v-btn>
    </v-toolbar>

    <v-content>
      <Main />
    </v-content>
  </v-app>
</template>

<script>
import Main from "./components/Main";

export default {
  name: "App",
  components: {
    Main
  },
  data() {
    return {
      //
    };
  }
};
</script>
