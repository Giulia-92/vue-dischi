
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