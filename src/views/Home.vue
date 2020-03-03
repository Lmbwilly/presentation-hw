/* eslint-disable max-len */
<template>
  <div class="home">
    <v-card color="orange lighten-4">
      <v-card-title class="text-center justify-center py-6">
        <h1 class="font-weight-bold display-2 secondary--text text--lighten-1">
          How to easily make a Website
        </h1>
      </v-card-title>
      <v-card-text>
        <v-tabs v-model="tab" color="orange" grow>
          <v-tab v-for="item in items" :key="item">
            {{ item }}
          </v-tab>
        </v-tabs>

        <v-tabs-items v-model="tab">
          <v-tab-item :key="items[0]">
            <v-card color="orange" class="lighten-1" flat tile>
              <v-card-text class=" font-weight-medium white--text">
                <v-row>
                  <v-col shrink>
                    <v-img
                      width="200"
                      alt="Vue logo"
                      :src="require('@/assets/vue_logo.png')"
                    />
                  </v-col>
                  <v-col gow>fhuishjjhsjk </v-col>
                </v-row>
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      tab: null,
      items: ["Introduction", "Entrees", "Deserts", "Cocktails"]
    };
  }
};
</script>
