<template>
  <div>
    <v-card style="margin-right:5%;margin-left:5%;margin-top:5%;background-color:grey">
      <br>
      <h2 style="text-align:center;margin-top:2%">ABOUT</h2>

      <v-simple-table style="width:50%;height:40%;margin-left:45%;margin-top:1%;margin-bottom:5%">
        <template v-slot:default>
          <thead>
            <tr></tr>
          </thead>
          <tbody>
            <tr v-for="item in personalInfo" :key="item.field1">
              <td>{{ item.field1 }}</td>
              <td>{{ item.info }}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
      <br>

      <div style="float:left;margin-top:-25%;margin-left:10%">
        <v-avatar size="250" style="margin-left:15%;position:relative;margin-top:-40%">
          <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
        </v-avatar>
        <h1 style="position:relative;margin-top:5%">Mellyne Grace Nadela</h1>
      </div>
    </v-card>

    <template >
      <v-row style="width:90%;margin-left:5%;margin-right:5%;margin-top:5%">
        
        <v-col >
          <v-card >
            <v-container fluid>
                <h2>My Porfolio</h2>
              <v-row>
                    
                <v-col v-for="n in 9" :key="n" class="d-flex child-flex" cols="4">
                  <v-card flat tile class="d-flex">
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="grey lighten-2"
                    >
                      <template v-slot:placeholder>
                        <v-row class="fill-height ma-0" align="center" justify="center">
                          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-row>
                      </template>
                    </v-img>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </div>
</template>
 
    

  
  


  
    
  

<script>
export default {
  data() {
    return {
      personalInfo: [
        {
          field1: "Address",
          info: "Lumapao"
        },
        {
          field1: "Email",
          info: "Mellyne@gmail.com"
        },
        {
          field1: "Contact",
          info: "09756818441"
        },
        {
          field1: "Event",
          info: "Wedding"
        },
        {
          field1: "Number Of Events",
          info: 6
        },
        {
          field1: "Package",
          info: "Free Photo Album"
        },
        {
          field1: "Range",
          info: "90,000 - 100,000"
        }
      ]
    };
  }
};
</script>