<template>
<div>
<div 
 v-for="(item,index) in cardList" :key="index" :img="item.poster" :name="index.author" :type="index.genre" :album="index.title" :age="index.year"></div>
</div>
    
</template>
<script>
import axios from 'axios';
export default {
 name:'DischiContent',
 data(){
    return{
        cardList:[],
      apiPath:'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },
  created(){
       console.log(this.apiPath)
      axios.get(this.apiPath).then((res)=>{
          console.log(this.apiPath)
          this.cardList =res.data.response
          console.log (res.data.response)
          
      })
  }
}
</script>
<style>
main{
  background-color: rgb(24, 23, 23);
  width: 100%;
  height:100vh;
}
</style>