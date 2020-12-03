<template>
  <div class="marginer">
      <h1>Contact Us</h1>
      <v-form>
        <v-text-field
        v-model="email"
        :counter="100"
        label="E-Mail"
        required
        ></v-text-field>
        <v-container fluid>
          <v-textarea
          name="message"
          filled
          label="Message"
          auto-grow
          ></v-textarea>
        </v-container>
      </v-form>
  </div>
</template>

<script>
export default {

}
</script>

<style>
@media screen  and (min-width : 700px) {
  .marginer{
    margin-left: 20%;
    margin-right:20%
  }
}
</style>