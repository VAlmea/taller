<template>
  <v-main>
    <NavBar />
    <v-container>
      <slot/>
    </v-container>
  </v-main>
</template>

<script>
import NavBar from "../NavBar";
export default {
  components: {
    NavBar,
  },
};
</script>

<style>
</style>