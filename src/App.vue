<template>
  <v-app>
    <Header v-if="loginNa()" />
    <router-view />
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",

  components: {
    Header
  },

  data: () => ({
    //
  }),
  methods: {
    loginNa() {
      if (this.$route.path == "/personalAccount") {
        return false;
      }
       else if (this.$route.path == "/updateporfolio") {
        return false;
      } 
      else if (this.$route.path == "/viewporfolio") {
        return false;
      } else {
        return true;
      }
    }
  }
};
</script>
