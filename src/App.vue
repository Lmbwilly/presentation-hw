<template>
  <v-app>
    <v-app-bar app color="grey lighten-3">
      <div class="d-flex align-center">
        <router-link to="/">
          <v-img
            alt="its Logo"
            class="shrink mr-2"
            contain
            :src="require('@/assets/its_logo.png')"
            transition="scale-transition"
            min-width="120"
            width="120"
          />
        </router-link>
      </div>

      <v-spacer></v-spacer>

      <v-btn to="sandbox" outlined color="orange">
        <span class="mr-2">Sandbox</span>
        <v-icon>mdi-code-braces</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  })
};
</script>
