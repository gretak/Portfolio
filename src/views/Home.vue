<template>
  <div class="home">
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
