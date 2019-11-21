<template>
  <v-app class="form" id="inspire">
    <v-content>
      <v-container style="margin-left:30%">
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="secondary" dark flat>
                <v-toolbar-title>SIGNUP</v-toolbar-title>
                <v-spacer />
              </v-toolbar>
              <v-card-text>
                <template>
                  <v-form ref="form" v-model="valid" :lazy-validation="lazy">
                    <v-text-field v-model="name" :rules="nameRules" label="Name" required></v-text-field>
                    <v-text-field v-model="address" :rules="nameRules" label="Address" required></v-text-field>
                    <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
                    <v-text-field v-model="password" :rules="passwordRules" label="Password" type="password" required></v-text-field>
                    <v-text-field v-model="contact" :rules="numberRules" label="Contact Number" type="number" min=0 required></v-text-field>
                    <v-text-field v-model="price"  label="Price" type="number" min=1 required></v-text-field>
                    <v-text-field v-model="packages" :rules="packageRules" label="Package" required></v-text-field>
                    <v-text-field v-model="photo"  label="Photo" type="file" required></v-text-field>
                  </v-form>
                </template>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn class="mr-4" @click="submit">submit</v-btn>
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
  props: {
    source: String
  },
  data: () => ({
    valid: true,
    name: "",
    nameRules: [
      v => !!v || "Name is required",
      v => (v && v.length <= 10) || "Name must be less than 10 characters"
    ],
    contact:"",
    numberRules:[
      v=>!!v||"Contact Number is required",
      v => (v && v.length <= 11 ) || "Name must be less  11 numbers",
       v => (v && v.length >= 11 ) || "Name must be less  11 numbers",
      

    ],
    packages:"",
    packageRules:[
      v=>!!v||"Package is important"
    ],
    password:"",
    passwordRules:[
       v => !! v ||"password  is required",
      v => (v && v.length >= 8 ) || "Name must be less  8 numbers",


    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ],
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
    lazy: false
  }),

  methods: {
    validate() {
      if (this.$refs.form.validate()) {
        this.snackbar = true;
      }
    },
    reset() {
      this.$refs.form.reset();
    },
    resetValidation() {
      this.$refs.form.resetValidation();
    }
  },
  // data() {
  //   return {
  //     name: "",
  //     address: "",
  //     email: "",
  //     password: "",
  //     contact: "",
  //     event: "",
  //     range: "",
  //     packages: "",
  //     photoUp: ""
  //   };
  // },
  method: {
    signup() {}
  }
};
</script>
<style scoped>
</style>
