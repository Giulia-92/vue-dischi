<template>
<main>
<div class="container">
  
  <div class="row">
    <DischiContent v-for="(item,index) in cardList" :key="index" class="col-6 col-md-4 col-lg-3 mb-3" :img="item.poster" :name="item.author" :type="item.genre" :album="item.title" :age="item.year"/>
 </div>
</div>
 </main>
</template>
<script>
import axios from 'axios';
import DischiContent from './DischiContent.vue';

export default {
 name:'MainContent',
  components: {
    DischiContent,
   
  },
 data(){
    return{
      SearchText:'',
      cardList:[],
      apiPath:'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },
  methods:{
    setSearchText(txt){
      this.SearchText = txt;
    }
    
  },
  computed:{
    filteredList(){
      if(this.SearchText !== ''){
        return this.characterList.filter((el)=>el.name.toLowercase().includes(this.searchText.toLowercase()))
      }else{
        return this.characterList
        
      }
      
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