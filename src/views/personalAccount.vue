<template>
  <div>
    <v-system-bar color="deep-purple darken-3"></v-system-bar>

    <v-app-bar color="grey accent-4" dark prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
<h2 style="float:left">ABout</h2>

      <v-spacer></v-spacer>
      
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute bottom temporary height="60%">
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-avatar size="100" style="margin-left:30%">
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
          </v-avatar>
          <center>
            <h2>WeOrg!</h2>
          </center>
          <br>

          <hr>

          <v-list-item>
            <router-link to="/viewporfolio">VIEW PORFOLIO</router-link>
          </v-list-item>

          <v-list-item>
            <router-link to="/updateporfolio">UPDATE PORFOLIO</router-link>
          </v-list-item>
          <v-list-item>
            <router-link to="/">LOGOUT</router-link>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  name: "personalAccount",
  data: () => ({
    drawer: false,
    group: null,
    items: [
      {
        title: "Birthday",
        to: "/Birthday "
      },
      {
        title: "Burial",
        to: "/Burial"
      },
      {
        title: "Baptist",
        to: "/Baptist"
      },
      {
        title: "Wedding",
        to: "/Wedding"
      }
    ]
  }),

  watch: {
    group() {
      this.drawer = false;
    }
  }
};
</script>


