<template>
  <div>
    <v-system-bar color="deep-purple darken-3"></v-system-bar>

    <v-app-bar color="deep-purple accent-4" dark prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute bottom temporary height="50%">
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-avatar size="100" style="margin-left:30%">
         

            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
          </v-avatar>
          <center><h2>WeOrg!</h2></center>
           <br> 

          <hr>

          <v-list-item>
            <router-link to="/Home">HOME</router-link>
          </v-list-item>

          <v-list-item>
            <router-link to="/About">ABOUT</router-link>
          </v-list-item>

          <div>
            <v-menu>
              <template v-slot:activator="{ on }">
                <v-btn dark v-on="on">CATEGORIES</v-btn>
              </template>
              <v-list>
                <v-list-item v-for="(item, index) in items" :key="index">
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
          <v-list-item>
            <router-link to="/Login">LOGIN</router-link>
          </v-list-item>
          <v-list-item>
            <router-link to="/Signup">SIGNUP</router-link>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
    items: [
      { title: "Birthday" },
      { title: "Burial" },
      { title: "Baptist" },
      { title: "Wedding" }
    ]
  }),

  watch: {
    group() {
      this.drawer = false;
    }
  }
};
</script>


