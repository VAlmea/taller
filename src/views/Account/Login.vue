<template>
  <v-row justify="center" >
    <v-col class="col-md-4">
      <v-card elevation="10" outlined>
        <v-card-title> Login </v-card-title>
        <h1>login</h1>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
    created(){
        this.$emit(`update:layout`, "LoginLayoutVue")
    }
};
</script>

<style>
</style>