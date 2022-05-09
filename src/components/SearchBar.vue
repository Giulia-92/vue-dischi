<template>
    <div>
  <div class="input-group">
  <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" v-model='inputText' @keyup.enter=$emit('search',inputText)>
  <button class="btn btn-outline-secondary" type="button" @click="$emit('search',inputText)">Filtra</button>
</div>
    </div>
</template>
<script>
export default {
   name:'SearchBar',
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
   }
}
</script>