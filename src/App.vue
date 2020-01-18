<template>
  <v-app>
    <v-content>
      <v-container fluid class="teal accent-6 white--text">
        <v-row>
          <v-container>
            <v-row>
              <v-col cols="8">
                <h1 class="title">
                  Welcome to my portfolio site, it contains a list of current
                  projects and information about me.
                </h1>
              </v-col>
              <v-col cols="4">
                will be icons here
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

      <v-container fluid class="teal lighten-2 white--text">
        <v-row>
          <v-container class="teal lighten-2 mt-n12" style="z-index:1">
            <v-col cols="12" class="pt-5">
              <div class="title	 white--text">
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
                  <li>
                    Sometimes I can not sleep till ~2 am and I can gather so
                    many cool ideas/projects I will start the next day. <br />I
                    forget them in the morning.
                  </li>
                </ul>
                <p class="pt-5">
                  I am enjoying my job if I learn, help and get recognised for
                  my hard work. I believe I have multiple skills and always like
                  to challenge myself, it is the only way of learning. I am
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
        <row>
          <v-banner class="teal accent-5 white--text pa-3 mb-10 mt-10">
            Contact me
          </v-banner>
        </row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import CardsList from "./components/CardsList";

export default {
  name: "App",

  components: {
    CardsList
  },

  data: () => ({
    //
  })
};
</script>
