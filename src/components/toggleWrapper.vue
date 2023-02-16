<template>
<div class="toggle-wrapper">
    <img  class='whiteicon' :src="logo"/>
    <label class="toggle">
       <input type="checkbox" :checked ="(mode === 'dark') ? 'checked' : false" @change="$emit('toggle')"/>
      <span class="toggler round"></span>
    </label>

       </div>
</template>

<script>

       export default {
           props:['mode'],
           data(){
              return{
                     logo:require('../assets/icons8-sun-48-w.png')
              }
           } 
       }

</script>

<style scoped>
.toggle{
position:absolute;
display: inline-block;
width:60px;
height:34px;
background: #ff0000;
}

.toggler{
       position: absolute;
       top:0;
       left:0;
       right: 0;
       bottom:0;
       background: #153515;
       -webkit-transition:0.4s ;
       transition: 0.4s;
}
.toggler::before{
       position: absolute;
       content: "";
       height:26px;
       width:26px;
       left:4px;
       bottom:4px;
       background: #ff0000;
}
input:checked + .toggler{
       background: #2196f3;
}
input:focus + toggler{
       box-shadow: 0 0 2px #2196f3;
}
input:checked + .toggler::before{
       -webkit-transform: translateX(26px);
       -ms-transform: translateX(26px);
       transform: translateX(26px);
}

</style>