<template>
  <v-app>
    <v-content>
      <v-container>
        <v-row>
          <CardsList />
        </v-row>
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
