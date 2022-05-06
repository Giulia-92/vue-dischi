<template>
    <div>{{name}} -{{type}} -{{album}} -{{age}}
   <img :src="img" :alt="name">
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
