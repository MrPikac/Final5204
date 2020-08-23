<template>
  <div class="about">
    <v-container>
      <v-row justify="center">
        <v-col cols="8" align-self="center">
          <h1>This is an about page</h1>
          <p>The company was founded in early 2004 with only two employees. Little by little the number of projects they did grew exponentially. Now when the firm has astableshed itself as one of the top civil engenering firms in Novi Sad, buisness is booming</p>
        </v-col>  
      </v-row>

      <v-row justify="center">
        <v-col cols="5" align-self="center">
          <v-img src="@/assets/images/architecture-828596_1920.jpg" alt="Tall glass building" max-height="450px" min-height="150px" max-width="450px" min-width="150px"></v-img>
        </v-col>
      </v-row>
    </v-container>

    <v-row justify="center">
      <v-col cols="8" align-self="center">
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid nobis aperiam neque mollitia dolor libero sit corporis eveniet sapiente debitis provident quae ut consectetur tempore voluptatum, ad officia magni nulla?</p>
      </v-col>
    </v-row>
  </div>
</template>





<style lang="scss">
$color: #CCF0FF;
.about {
  background-color: $color;
}
</style>