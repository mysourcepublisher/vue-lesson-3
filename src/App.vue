<template>
    <v-app>
      <v-app-bar color="primary" app dark>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" ></v-app-bar-nav-icon>
        <v-toolbar-title>Simple Advertiser</v-toolbar-title>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" absolute bottom temporary >
      <v-list nav dense >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item to="/">
            <v-list-item-icon >
               <v-icon>mdi-home-outline</v-icon> 
            </v-list-item-icon>
            <v-list-item-content>
               <v-list-item-title>Home</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item to="/your">
            <v-list-item-icon>
               <v-icon>mdi-filter-variant</v-icon> 
            </v-list-item-icon>
            <v-list-item-content>
               <v-list-item-title>Your Ads</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

           <v-list-item to="/new">
            <v-list-item-icon>
               <v-icon>mdi-plus</v-icon> 
            </v-list-item-icon>
            <v-list-item-content>
               <v-list-item-title>Add New Ads</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

           <v-list-item to="/contact-us">
            <v-list-item-icon>
               <v-icon>mdi-account-box-outline</v-icon> 
            </v-list-item-icon>
            <v-list-item-content>
               <v-list-item-title>Contact Us</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

           <v-list-item to="/about">
            <v-list-item-icon>
               <v-icon>mdi-information-variant</v-icon> 
            </v-list-item-icon>
            <v-list-item-content>
               <v-list-item-title>About Us</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <router-view/>
    </v-main>
    </v-app>
 </template>

<script>
  export default {
    data: () => ({
      drawer: false,
      group: null,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>




<style lang="scss">
.purple{
  background: #6a1b90;
}
</style>
