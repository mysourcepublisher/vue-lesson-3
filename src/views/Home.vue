<template>
  <div id="app">
    <div class="ingr">
      <v-flex d-flex>
        <v-layout wrap>
          <v-flex md4 v-for="(ads,index) in ads" :key="index">
            <Card :title="ads.title" :image="ads.picture" about="none" :price="ads.price"/>
          </v-flex>
        </v-layout>
      </v-flex>
    </div>
  </div>
</template>

<script>
  import Card from '../components/card.vue'

  export default {
    data:()=>{
      return {
        ads:[
          {title:"Toy Car",picture:"toy-car.jpg",price:200.05},
          {title:"chocolate Cake",picture:"chocolate-cake.jpg",price:120.00},
          {title:"Cake 2",picture:"chocolate-cake.jpg",price:500.00},
          {title:"Toy Car",picture:"toy-car.jpg",price:200.00},
          {title:"Toy Car 2",picture:"toy-car.jpg",price:120.00},
          {title:"Ice Cream",picture:"ice-cream.jpg",price:500.00}
        ]
      }
    },
    name:'App',
    components:{
      Card
    }
  }
</script>

<style>
.ingredients{
}
</style>
