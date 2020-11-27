<template>
  <v-bottom-navigation
    color="teal"
    flat
    grow
    class="my-auto d-flex"
  >
    <v-btn class="my-auto">
      <span>Recents</span>
      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn class="my-auto">
      <span>Blog</span>

      <v-icon>mdi-comment-multiple-outline</v-icon>
    </v-btn>

    <v-btn class="my-auto" router-link to="/account/login">
      <span>Login</span>

      <v-icon>mdi-login</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>
<script>
  export default {
  }
</script>