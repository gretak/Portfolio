<template>
  <v-app>
    <v-content>
      <v-container fluid class="grey darken-3 white--text pa-0">
        <v-row>
          <v-container>
            <v-row align="center">
              <v-col cols="12" sm="8">
                <p class="pb-0">
                  Hello, my name is Greta. You are now visiting my personal
                  website, welcome! Here you can find a list of my current
                  projects and information about me.
                </p>
              </v-col>
              <v-col cols="12" sm="4" class="text-right">
                <v-btn
                  icon
                  dark
                  href="mailto:kavaliauskaite3@gmail.com"
                  target="_blank"
                  color="teal lighten-4"
                >
                  <v-icon dark large>email</v-icon>
                </v-btn>
                <v-btn
                  icon
                  dark
                  href="tel:+447402245731"
                  target="_blank"
                  class="ma-4"
                  color="teal lighten-4"
                >
                  <v-icon dark large>phone_enabled</v-icon>
                </v-btn>

                <v-btn
                  icon
                  dark
                  href="https://www.linkedin.com/pub/greta-kavaliauskaite/6a/6a6/2b1"
                  target="_blank"
                  color="teal lighten-4"
                >
                  <v-icon large>fab fa-linkedin</v-icon>
                </v-btn>
              </v-col>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
      <v-container fluid class="teal accent-5 white--text pa-0">
        <v-img
          class="white--text align-end"
          height="400"
          src="./assets/hero-image.png"
          width="100%"
        >
        </v-img>
      </v-container>

      <v-container fluid class="teal lighten-4 white--text mb-10">
        <v-row>
          <v-container class="teal lighten-2 mt-n12 mb-n12" style="z-index:1">
            <v-col cols="12" class="pt-5">
              <div class="white--text">
                <p>About me:</p>
                <ul>
                  <li>I will go for an easy, but robust solution.</li>
                  <li>
                    I have a degree in project management, I believe a good PM
                    should be technical.
                  </li>
                  <li>I am not a coding ninja, I am just working hard.</li>
                  <li>I am good with teaching/helping others.</li>
                  <li>I am empathic and easy to communicate with.</li>
                  <li>
                    I am respectful and treat people fairly, I am never unfair.
                  </li>
                </ul>
                <p class="pt-5">
                  I am enjoying my job if I learn, help and get recognised for
                  my hard work. I believe I have comprehensive skills and always
                  like to challenge myself, it is the only way of learning. I am
                  looking for a job where I am not looking forward to a weekend,
                  I enjoy everyday.
                </p>
              </div>
            </v-col>
          </v-container>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <CardsList />
        </v-row>

        <v-row>
          <v-flex xs12>
            <v-card-title class="headline mt-6 teal--text text--darken-2">
              Check these links</v-card-title
            >
          </v-flex>

          <v-col cols="12" class="teal accent-5 white--text pa-3 mb-5 mt-3">
            <v-btn
              medium
              class="ma-3 teal--text"
              color="white"
              v-on:click="downloadItem('./gretak-cv.pdf')"
            >
              download CV
            </v-btn>

            <v-btn
              medium
              class="ma-3 teal--text"
              color="white"
              href="https://github.com/gretak"
            >
              GitHub
            </v-btn>
            <v-btn
              medium
              class="ma-3 teal--text"
              color="white"
              href="https://www.codewars.com/users/gretak"
            >
              Code wars
            </v-btn>
            <v-btn
              medium
              class="ma-3 teal--text"
              color="white"
              href="https://www.artgallery.co.uk/artist/greta_kavaliauskaite"
            >
              Art gallery
            </v-btn>
            <v-btn
              medium
              class="ma-3 teal--text"
              color="white"
              href="https://www.youtube.com/watch?v=CA01cA2c7eA"
            >
              Youtube
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
      <v-container fluid class="pa-0 mt-5">
        <v-footer class="grey darken-3 text-center white--text ma-0">
          <v-col cols="12">
            <v-btn
              icon
              dark
              href="mailto:kavaliauskaite3@gmail.com"
              target="_blank"
              color="teal lighten-4"
            >
              <v-icon dark medium>email</v-icon>
            </v-btn>
            <v-btn
              icon
              dark
              href="tel:+447402245731"
              target="_blank"
              color="teal lighten-4"
            >
              <v-icon dark medium>phone_enabled</v-icon>
            </v-btn>

            <v-btn
              icon
              dark
              href="https://www.linkedin.com/pub/greta-kavaliauskaite/6a/6a6/2b1"
              target="_blank"
              color="teal lighten-4"
            >
              <v-icon dark medium>fab fa-linkedin</v-icon>
            </v-btn>
          </v-col>

          <v-col cols="12" class="pt-0">
            <div>
              Greta Kavaliauskaite &copy; {{ new Date().getFullYear() }}
            </div>
          </v-col>
        </v-footer>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import CardsList from "./components/CardsList";
import axios from "axios";

export default {
  name: "App",

  components: {
    CardsList
  },

  data: () => ({
    //
  }),

  methods: {
    downloadItem(fileName) {
      axios({
        url: fileName,
        method: "GET",
        responseType: "blob" // important
      }).then(response => {
        const url = window.URL.createObjectURL(new Blob([response.data]));
        const link = document.createElement("a");
        link.href = url;
        link.setAttribute("download", fileName);
        document.body.appendChild(link);
        link.click();
      });
    }
  }
};
</script>
