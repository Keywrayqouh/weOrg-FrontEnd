<template>
  <v-simple-table dark>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">Name</th>
          <th class="text-left">Calories</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in organizers" :key="item.name">
          <td>{{ item.name }}</td>
          <td>{{ item.address }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>
<script>
  export default {
    data () {
      return {
        organizers: [
          {
            name: 'Mellyne Grace R. Nadela',
            address: "Brgy. Lumapao, Canlaon City",
          },
          {
            name: 'Lorly Sugal',
            address: "South Cotabato",
          },
          {
            name: 'Jakeniel R. Erim',
            address: "Brgy. Lumapao, Canlaon City",
          },
          {
           name: 'Princess Joy Duran',
            address: "Talamban, Cebu City",
          },
          {
            name: 'Keywray Qouh',
            address: "Guihulngan City",
          },
          {
            name: 'Sharmen Claire',
            address: "Brgy. Pula, Canlaon City",
          },
          {
            name: 'Christian Gigante',
            address: "Daan Bantayan",
          },
          {
            name: 'Ivy Joy Devilleres',
            address: "Bukidnon",
          },
          {
            name: 'Jane Repollo',
            address: "Tanjay, Dumaguete City",
          },
          {
            name: 'Leonilo Torre Jr.',
            address: "San Carlos City"
          },
        ],
      }
    },
  }
</script>