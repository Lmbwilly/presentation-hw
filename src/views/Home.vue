/* eslint-disable max-len */
<template>
  <div class="home">
    <v-row justify="center">
      <v-col cols="8">
        <v-card color="orange lighten-4">
          <v-card-title class="text-center justify-center py-6">
            <h1
              class="font-weight-bold display-2 secondary--text text--lighten-1"
            >
              How to easily make a Website
            </h1>
          </v-card-title>
          <v-card-text>
            <v-tabs v-model="tab" color="orange" grow>
              <v-tab v-for="item in items" :key="item">
                {{ item }}
              </v-tab>
            </v-tabs>

            <v-tabs-items class="grey lighten-2" v-model="tab">
              <v-tab-item :key="items[0]">
                <v-card color="grey" class="lighten-2" flat tile>
                  <v-card-text class="font-weight-medium">
                    <v-row justify="space-around">
                      <v-col cols="2">
                        <v-img
                          width="200"
                          alt="Vue logo"
                          :src="require('@/assets/vue_logo.png')"
                        />
                      </v-col>
                      <v-col cols="8" class="body-1">
                        <ul>
                          <li>
                            Using Vue as a lightweight JavaScript-Framework
                            (33KB)
                          </li>
                          <li>Well documented - Good to learn</li>
                          <li>Easy to install</li>
                          <li>
                            Well-known enterprises are using Vue, for example
                            Nintendo for <kbd>my.nintendo.com</kbd>
                          </li>
                        </ul>
                        <br />
                        <ul>
                          <li>
                            Use Vuetify for UI-components
                          </li>
                          <li>Great configurability</li>
                          <li>Big portfolio of components (82+)</li>
                          <li>Similar grid-system as Bootstrap</li>
                          <li>No need to do styling by yourself</li>
                        </ul>
                      </v-col>
                      <v-col cols="2">
                        <v-img
                          width="200"
                          alt="Vuetify logo"
                          :src="require('@/assets/vuetify_logo.png')"
                        />
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item :key="items[1]">
                <v-row align="center">
                  <v-col class="text-center" cols="12" sm="3">
                    <div class="my-2">
                      <v-btn text small>Normal</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text small color="primary">Primary</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text small color="error">Error</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text small disabled>Disabled</v-btn>
                    </div>
                  </v-col>

                  <v-col class="text-center" cols="12" sm="3">
                    <div class="my-2">
                      <v-btn>Normal</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn color="primary">Primary</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn color="error">Error</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn disabled>Disabled</v-btn>
                    </div>
                  </v-col>

                  <v-col class="text-center" cols="12" sm="3">
                    <div class="my-2">
                      <v-btn text outlined large>Normal</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text outlined large color="primary">Primary</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text outlined large color="error">Error</v-btn>
                    </div>
                    <div class="my-2">
                      <v-btn text outlined large disabled>Disabled</v-btn>
                    </div>
                  </v-col>
                  <v-col cols="12" sm="3">
                    <div class="text-center">
                      <div class="my-2">
                        <v-btn color="secondary" fab x-small dark>
                          <v-icon>mdi-television</v-icon>
                        </v-btn>
                      </div>
                      <div class="my-2">
                        <v-btn color="primary" fab small dark>
                          <v-icon>mdi-pencil</v-icon>
                        </v-btn>
                      </div>
                      <div class="my-2">
                        <v-btn color="warning" fab dark>
                          <v-icon>mdi-account-circle</v-icon>
                        </v-btn>
                      </div>
                      <div class="my-2">
                        <v-btn color="error" fab large dark>
                          <v-icon>mdi-alarm</v-icon>
                        </v-btn>
                      </div>
                      <div class="my-2">
                        <v-btn color="success" fab x-large dark>
                          <v-icon>mdi-domain</v-icon>
                        </v-btn>
                      </div>
                    </div>
                  </v-col>
                </v-row>
              </v-tab-item>
              <v-tab-item :key="items[2]">
                <v-card max-width="400" class="mx-auto">
                  <v-system-bar color="pink darken-2" dark>
                    <v-spacer></v-spacer>
                    <v-icon>mdi-window-minimize</v-icon>
                    <v-icon>mdi-window-maximize</v-icon>
                    <v-icon>mdi-close</v-icon>
                  </v-system-bar>

                  <v-app-bar dark color="pink">
                    <v-app-bar-nav-icon></v-app-bar-nav-icon>
                    <v-toolbar-title>Music</v-toolbar-title>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-magnify</v-icon>
                    </v-btn>
                  </v-app-bar>

                  <v-container>
                    <v-row dense>
                      <v-col cols="12">
                        <v-card color="#385F73" dark>
                          <v-card-title class="headline"
                            >Unlimited music now</v-card-title
                          >
                          <v-card-subtitle
                            >Listen to your favorite artists and albums whenever
                            and wherever, online and offline.</v-card-subtitle
                          >
                          <v-card-actions>
                            <v-btn text>Listen Now</v-btn>
                          </v-card-actions>
                        </v-card>
                      </v-col>

                      <v-col
                        v-for="(cardItem, i) in cardItems"
                        :key="i"
                        cols="12"
                      >
                        <v-card :color="cardItem.color" dark>
                          <div
                            class="d-flex flex-no-wrap justify-space-between"
                          >
                            <div>
                              <v-card-title
                                class="headline"
                                v-text="cardItem.title"
                              ></v-card-title>

                              <v-card-subtitle
                                v-text="cardItem.artist"
                              ></v-card-subtitle>
                            </div>

                            <v-avatar class="ma-3" size="125" tile>
                              <v-img :src="cardItem.src"></v-img>
                            </v-avatar>
                          </div>
                        </v-card>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      tab: null,
      items: ["Introduction", "Diversity", "Example"],
      cardItems: [
        {
          color: "#1F7087",
          src: "https://cdn.vuetifyjs.com/images/cards/foster.jpg",
          title: "Supermodel",
          artist: "Foster the People"
        },
        {
          color: "#952175",
          src: "https://cdn.vuetifyjs.com/images/cards/halcyon.png",
          title: "Halcyon Days",
          artist: "Ellie Goulding"
        }
      ]
    };
  }
};
</script>
