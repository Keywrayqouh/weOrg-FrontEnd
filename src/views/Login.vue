<template>
  <v-app class="form" id="inspire">
    <v-content>
      <v-container style="margin-top:-10%">
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="secondary" dark flat>
                <v-toolbar-title>LOGIN</v-toolbar-title>
                <v-spacer />
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field
                    v-model="username"
                    label="Email"
                    name="login"
                    prepend-icon="mdi-account"
                    type="text"
                  ></v-text-field>
                  <v-text-field
                    v-model="password"
                    id="password"
                    label="Password"
                    name="password"
                    prepend-icon="mdi-lock"
                    type="password"
                  ></v-text-field>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn v-on:click="login" color="secondary">Login</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>


<script>
export default {
  name: "btnLogin",
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    login() {
      if (this.username == "admin@gmail.com" && this.password == "admin") {
        this.$router.push({ name: "personalAccount" });
      } else {
        alert("Invalid credentials");
      }
    }
  },
  props: {}
};
</script>
<style scoped>
.form {
  margin-top: 20%;
}
</style>
