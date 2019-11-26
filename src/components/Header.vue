<template>
  <div>
    <v-system-bar color="grey"></v-system-bar>

    <v-app-bar color="grey" dark prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute bottom temporary height="60%">
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-avatar size="100" style="margin-left:30%">
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
          </v-avatar>
          <center>
            <h2>WeOrg!</h2>
          </center>
          <br />

          <hr />

          <v-list nav>
            <v-list-item link>
              <v-list-item-icon></v-list-item-icon>
              <v-list-item-title @click="goto('/Home')">HOME</v-list-item-title>
            </v-list-item>
            <v-list-item link>
              <v-list-item-icon></v-list-item-icon>
              <v-list-item-title @click="goto('/About')">About us</v-list-item-title>
            </v-list-item>
            <v-menu>
              <template v-slot:activator="{ on }">
                <v-btn dark v-on="on">CATEGORIES</v-btn>
              </template>
              <v-list>
                <v-list-item >
                   <v-list-item-title> <router-link to="/Concert" >Concert</router-link></v-list-item-title>
                   
                 
                  <router-link to="/Birthday">Birthday</router-link>
                  <router-link to="/Graduation">Graduation</router-link>
                  <router-link to="/Wedding">Wedding</router-link>
                </v-list-item>
              </v-list>
            </v-menu>
            <v-list-item link>
              <v-list-item-icon></v-list-item-icon>
              <v-list-item-title @click="goto('/Login')">LOGIN</v-list-item-title>
            </v-list-item>
            <v-list-item link>
              <v-list-item-icon></v-list-item-icon>
              <v-list-item-title @click="goto('/Signup')">SIGNUP</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
   name: 'Sidebar',
  methods:{
      goto(link){
        this.$router.push({path:link});
      }
    },
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
<style scoped>
li {
  display: block;
}

li:hover {
  color: red;
}
</style>



