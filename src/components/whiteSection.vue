<template>
  <div class="linksBtn">
   

   <a href="#">About</a>
   <a href="#">Settings</a>
   <a href="#">Help</a>

   <button>Go to App</button>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>

  div{
    background: white;
    width:350px;
    margin:0px auto;
    height:35vh;
  }
  .linksBtn{
    display:flex;
    flex-direction: column;
    text-align: center;
   padding-top: 20px;
   font-size: 20px;
  }
 button{
    width:200px;
   margin: auto;
   border: none;
    padding: 10px;
  }
  button:hover{
    background: blue;
    color:#ffffff;

  }
  a{
    text-decoration: none;
    padding-bottom: 20px;
    color:rgb(34, 34, 34)
  }
  a:hover{
    color:grey;
  }
</style>