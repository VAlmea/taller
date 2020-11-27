<template>
  <v-app class="v-flex">
   <component :is="layout">
     <router-view :layout.sync="layout"></router-view>
   </component>   
  </v-app>
</template>

<script>
import Principal from './components/Layouts/PrincipalLayout';
import Login from './components/Layouts/LoginLayout';
import Admin from './components/Layouts/AdminLayout';
export default {
  components:{
    Principal,
    Login,
    Admin
  },
  name: 'App',
  data: () => ({
    layout:'Principal'
  }),
};
</script>
