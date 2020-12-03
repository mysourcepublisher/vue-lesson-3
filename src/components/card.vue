<template>
  <div class="app">
      <v-card max-width="400" class="mx-auto">
          <v-img v-bind:src="require('../assets/'+image)" height="200px"></v-img>
          <v-card-title>{{ title }}</v-card-title>
          <v-card-subtitle>{{price}}</v-card-subtitle>
          <v-card-actions>
              <v-btn color="purple" text>Contact</v-btn>
              <v-spacer></v-spacer>
              <v-btn icon @click="show = !show">
                  <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
              </v-btn>
          </v-card-actions>
          <v-expand-transition>
              <div v-show="show">
                  <v-divider></v-divider>
                  <v-card-text>
                      {{about}}
                  </v-card-text>
              </div>
          </v-expand-transition>
      </v-card>
  </div>
</template>

<script>
export default {
    name:'Card',
    props:{
        title:String,
        image:String,
        about:String,
        price:Number
    },
    data:()=>({
        show:false,
    }),
}
</script>

<style>

</style>