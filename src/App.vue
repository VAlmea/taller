<template>
  <v-app class="v-flex">
    <component :is="layout">
      <router-view :layout.sync="layout"></router-view>
    </component>
  </v-app>
</template>

<script>
import Principal from "./components/Layouts/PrincipalLayout";
import Login from "./components/Layouts/LoginLayout";
import Admin from "./components/Layouts/AdminLayout";
export default {
  components: {
    Principal,
    Login,
    Admin,
  },
  name: "App",
  data: () => ({
    layout: "Principal",
    location: null,
    gettingLocation: false,
    errorStr: null,
  }),
  created() {
            console.log("Hola")

    //do we support geolocation
    if (!("geolocation" in navigator)) {
      this.errorStr = "Geolocation is not available.";
      return;
    }

    this.gettingLocation = true;
    // get position
    navigator.geolocation.getCurrentPosition(
      (pos) => {
        this.gettingLocation = false;
        this.location = pos;
      },
      (err) => {
        this.gettingLocation = false;
        this.errorStr = err.message;
      },
    );
  },
};
</script>
