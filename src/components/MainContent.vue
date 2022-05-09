<template>
<main>
<div class="container">
 <DischiContent v-for="(item,index) in cardList" :key="index" :img="item.poster" :name="item.author" :type="item.genre" :album="item.title" :age="item.year"/>
</div>
 </main>
</template>
<script>
import axios from 'axios';
import DischiContent from './DischiContent.vue';
export default {
 name:'MainContent',
  components: {
    DischiContent
  },
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
}
.container{
 display:flex;
 flex-wrap: wrap;
 color: white;
 font-family: Arial, Helvetica, sans-serif;
}
</style>