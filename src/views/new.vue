<template>
  <div class="hello">
    <v-form >
    <v-text-field
    v-model="name"
    :counter="100"
    :rules="nameRules"
    label="Title"
    required
    ></v-text-field>
    <v-file-input
    :rules="rulesFile"
    accept="image/png, image/jpg, image/jpeg, image/bmp"
    placeholder = "Pick an image"
    prepend-icon="mdi-camera"
    label="Image"></v-file-input>
    <v-container fluid>
      <v-textarea
      name="about"
      filled
      label="About Description"
      auto-grow
      ></v-textarea>
    </v-container>
     <v-text-field
    v-model="price"
    :counter="10"
    label="Price"
    required
    ></v-text-field>
    <v-btn color="primary" dark>
      <v-icon>mdi-plus</v-icon>
      Add</v-btn>
  </v-form>
  </div>
</template>

<script>
export default {
  data: ()=>({
    valid:true,
    name:'',
    nameRules:[
      v => !! v || 'Name is required!',
      v => ( v && v.length <= 100 ) || 'Name must be less than 10 characters',
    ],
    rulesFile: [
      value => ! value || value.size < 2000000 || 'Avatar size shoulde be minimize',
    ],
  })
}
</script>

<style>
@media screen  and (min-width : 700px) {
  .hello{
    margin-left: 20%;
    margin-right:20%
  }
}
</style>