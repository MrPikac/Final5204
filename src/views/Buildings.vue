<template>
  <div class="buildings">
    <v-container>
      <v-row justify="center">
        <v-col cols="8" align-self="center">
          <h1>This is the Buildings page</h1>
          <p>Here we can show you the statistics of some of our most famous buildings</p>
        </v-col>
      </v-row>

      <v-row justify="center">
        <v-col cols="8" align-self="center">
            <v-simple-table fixed-header="true">
              <table>
                  <tr>
                    <th>Location</th>
                    <th>Area</th>
                    <th>Height</th>
                    <th>Parcel Area</th>
                  </tr>
                  <tr>
                    <td>Joakima Vujica 12</td>
                    <td>116m2</td>
                    <td>50m</td>
                    <td>200m2</td>
                  </tr>  
              </table>
            </v-simple-table>
        </v-col>
      </v-row>  


        <v-row justify="center">
          <v-col cols="5" align-self="center">
            <v-img src="@/assets/images/building-768815_1920.jpg" alt="Tall glass building" max-height="450px" min-height="150px" max-width="450px" min-width="150px"></v-img>
          </v-col>
      </v-row>

      <v-row justify="center">       
        <v-col cols="8" align-self="center"> 
            <v-form>
              <v-text-field outlined label="Comments"> </v-text-field>
            </v-form> 
          </v-col> 
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';
Vue.use(VueAxios, axios)
window.axios = require('axios');
  export default {
    name: 'Buildings',

      // mounted() {
      //   Vue.axios.get('https://jsonplaceholder.typicode.com/posts')
      //   .then((resp) =>{
      //     console.log(resp);
      //   })
      // },



      // mounted: function() {
      // axios.get('https://jsonplaceholder.typicode.com/posts')
      // .then(response => console.log(response));
    // },

    data: () => ({
      Location: [
        'Joakima Vujica 12',
      ],
      Area: [
        '116m2',
      ],
      Height: [
        '50m',
      ],
      Parcel_area: [
        '200m2'
      ]

    }),

      mounted () {
    axios
      .get('http://localhost:3306/api/buildings')
      .then(response => (this.info = response))
      }
  }
</script>




<style lang="scss">
$color: #CCF0FF;
.buildings {
  background-color: $color;
}

table {
  background-color: $color;
}
</style>