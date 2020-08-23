<template>
  <div class="log">
    <v-container>
      <v-row justify="center">
        <v-col cols="8" align-self="center">
            <h1>This is the Log in page and the Register page</h1>
        </v-col>
      </v-row>
        <v-row justify="center">
            <v-col cols="8" align-self="center">
                <h3>Register here</h3>
            </v-col>
        </v-row>
      <v-row justify="center">
          <v-col cols="8" align-self="center">
              <v-form @submit.prevent="submitForm">
                <v-text-field outlined label="First name" autofocus="true"> </v-text-field>
                <v-text-field outlined label="Last name"> </v-text-field>
                <v-text-field outlined label="Email"></v-text-field>
                <v-text-field outlined label="Password"></v-text-field>
                <v-btn outlined>Send</v-btn>
              </v-form>
          </v-col>
      </v-row>

      <v-row justify="center">
          <v-col cols="8" align-self="center">
              <h3>Log in here</h3>
          </v-col>
      </v-row>
      <v-row justify="center">
          <v-col cols="8" align-self="center">
              <v-form>
                <v-text-field outlined label="First name"></v-text-field>
                <v-text-field outlined label="Password"></v-text-field>
                <v-btn outlined>Send</v-btn>
              </v-form>
          </v-col>
      </v-row>
    </v-container>

  </div>
</template>




<script>
export default {

  
  data () {
    return {
        form: {
        FirstName: null,
        LastName: null,
        Email: null,
        Password: null
      }
    }
  },

methods: {
    isEmailValid: function() {
      return (this.email == "")? "" : (this.reg.test(this.email)) ? 'has-success' : 'has-error';
    }
  }
}
</script>


<style lang="scss">
$color: #CCF0FF;
.log {
  background-color: $color;
}
</style>