<template>
       <div>
         
          <Toggle :mode="mode" @toggle="$emit('toggle')"/> 
       </div>
</template>

<script>
import  Toggle from "./toggleWrapper.vue"
       export default {
           props:['mode'],
           components:{
              Toggle
           }   
       }
</script>

<style scoped>

</style>