<template>
<header>
    <img class="logo" src="../assets/Spotify.png" alt="Spotify">
      <div class="input-group">
  <input type="text" class="form-control" placeholder="Album name" aria-label="Album name" v-model='inputText' @keyup.enter="$emit('search',inputText)">
  <button class="btn btn-outline-secondary" type="button" @click="$emit('search',inputText)">Filtra</button>
</div>
</header>

</template>
<script>
export default {
   name:'HeaderContent',
   data(){
       return{
           inputText:'',
       }
   },
   methods:{
       reset(){
           this.inputText='';
           this.$emit('search',this.inputText)
       }
   }, 
}
</script>
<style scoped>
header{
    height:60px;
    background-color: rgb(67, 66, 66);
    width:100%;
    
}
.logo{
   
    width: 50px;
    float: left;
    margin-top:6px;
    margin-left:10px;
}
.form-control{
    background-color:rgb(54, 52, 52);
}
</style>
