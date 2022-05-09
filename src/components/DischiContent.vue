<template>
<div class="card mt-5" style="width: 18rem;">
  <img :src="img" class="card-img-top" :alt="name">
  <div class="card-body">
    <h1 class="card-title text center fw bold my-5">{{name}}</h1>
    <p class="card-text">
      {{type}} 
       {{album}} 
       {{age}}</p>
  </div>
</div>
</template>
<script>
export default {
  name: 'DischiContent',
  props:{
      name:String,
      type:String,
      img:Object,
      album:String,
      age:Number
     
  }
}
</script>
<style scoped>
.card{
  background-color: rgb(48, 48, 48);
  margin-top:2em;
  margin-right:1em;
  border-radius:10px;
  font-family:'Roboto Condensed',;
}
p{
  color:grey;
}
</style>
