<template>
  <div class="home">
    <v-banner single-line>
      We can't save your edits while you are in offline mode.
      <p>test</p>
    </v-banner>
    <CardsList />
  </div>
</template>

<script>
// @ is an alias to /src
import CardsList from "@/components/CardsList.vue";

export default {
  name: "home",
  components: {
    CardsList
  }
};
</script>
