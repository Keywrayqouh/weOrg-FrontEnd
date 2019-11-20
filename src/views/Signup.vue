<template>
  <v-app class="form" id="inspire">
    <v-content >
      <v-container style="margin-left:30%">
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="secondary" dark flat>
                <v-toolbar-title >SIGNUP</v-toolbar-title>
                <v-spacer/>
           </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field label="Name " name="name" type="text"/>
                  <v-text-field id="address" label="Address" name="address" type="text"/>
                   <v-text-field label="Email " name="email" type="email"/>
                  <v-text-field id="password" label="Password" name="password" type="password"/>
                   <v-text-field label="Contact Number " name="contact" type="number"/>
                  <v-text-field id="event" label="Event" name="event" type="text"/>
                    <v-text-field label="Range" name="range" type="number"/>
                  <v-text-field id="package" label="Package" name="package" type="text"/>
                   <v-text-field id="photo"  name="photo" type="file"/>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer/>
                <v-btn color="secondary">Login</v-btn>
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
  }
};
</script>
<style scoped>

</style>
