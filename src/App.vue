<template>
  <v-app>
    <Header />
    <v-main>
      <router-view></router-view>
    </v-main>

  <Footer />
  </v-app>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
  

window.axios = require('axios');
export default {
  name: 'App',
  components: { 
    Header, 
    Footer 
  },

  data: function() {
    return {
            //Comments that are under the table
            comments: [
                {
                  user: 'example',
                  text: 'lorem ipsum dolor lorem ipsum dolor lorem ipsum dolor',
                },
            ]
        }
    },

    methods: {
        submitComment: function(reply) {
            this.comments.push({
              text: reply
            });
        }
    }
};
</script>

<style lang="scss">
$color: #CCF0FF;
body {
  background-color: $color;
}
</style>