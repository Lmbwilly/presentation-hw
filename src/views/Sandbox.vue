<template>
  <div class="sandbox">
    <v-row justify="space-around">
      <v-col v-for="n in 10" :key="n" cols="12" sm="6" md="4">
        <v-card class="mx-auto" max-width="500" outlined>
          <v-img
            class="white--text align-end"
            height="200"
            :src="`https://picsum.photos/id/${n * 8}/400/200`"
          >
            <v-card-title>Hello, my first card</v-card-title>
          </v-img>
          <v-card-text>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex
            voluptatem, nam nihil magni laboriosam ea. Possimus voluptate illo
            ipsa ducimus eaque inventore earum numquam repudiandae molestiae!
            Eos tempora alias voluptatem?
          </v-card-text>
          <v-card-action>
            <v-btn text @click="snackbar = true" color="pink">Click Me</v-btn>
          </v-card-action>
        </v-card>
      </v-col>
    </v-row>
    <v-snackbar v-model="snackbar" color="error">
      {{ text }}
      <v-btn text @click="snackbar = false">
        Close
      </v-btn>
    </v-snackbar>
  </div>
</template>

<script>
// `https://picsum.photos/id/1/400/200`

export default {
  name: "Sandbox",
  components: {},
  data: () => ({
    snackbar: false,
    text: "Hello, I'm a snackbar"
  })
};
</script>
