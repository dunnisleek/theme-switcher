<template>
   
  <section :class="mode">
    
    <!-- <section> -->
   <HeaderCom/>
    <div class="wrapper">

   <!-- <HeaderCom :mode="mode" @toggle="toggle" /> -->
   
   <svg xmlns="http://www.w3.org/2000/svg" class="box" display="flex" width="45" height="45" viewBox="0 0 24 24" stroke-width="2" stroke="white" fill="none" stroke-linecap="round" stroke-linejoin="round">
   <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
   <path d="M4 4m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2z"></path>
   <path d="M9 15v2"></path>
   <path d="M12 11v6"></path>
   <path d="M15 13v4"></path>
</svg>
   
 
    
    <h1>Untercom <span>APP</span></h1>
    <p>Convert your hottest leads</p>
   </div>
   <whiteSection/>
   {{ isDark }}
   {{ toggleDark }}
  <br />
  <button @click="toggleDark">Toggle Dark Mode</button>
 
  </section>
</template>
   
<script >
import HeaderCom from './components/HeaderCom'
import whiteSection from './components/whiteSection.vue'
// import { useDark,useToggle} from '@vueuse/core';

    // const isDark = useDark();
      // const toggleDark = useToggle(isDark);
    



  export default {
 
    name:'app',
    components:{whiteSection, HeaderCom},

    data(){
      return{
     
        mode:'dark',
       
      
      }
    },
    
    methods:{
      toggle(){
        if(this.mode === 'dark'){
          this.mode === 'light'
          console.log(this.mode)
        }else if(this.mode ==='light'){
          this.mode ='dark'
          console.log(this.mode)
        }else{
          this.mode ='dark'
        }
        
      },
    
      
    }
  }

</script>

<style>
.box{
  margin: auto;
  display: flex;
}
body{
  height:100vh;
  margin: 0;
}
.dark{
  background: #282828;
  height: 100vh;
}
h1{
  color:#ffffff;
  text-align: center;
  font-size: 25px;
}
.wrapper{
  background: #3B81F6;
  width:350px;
  margin:0px auto 0px auto;
  height:30vh;
  padding-top: 20px;
 
}
h1 span{
  background: blue;
  padding: 10px;
  border-radius:5px ;
}
.wrapper p{
  color:#fff;
  text-align: center;
  padding-top: 15px;
}
[theme='dark'] {
  background: #252525;
  color: white;
}
[theme='dim'] {
  background: gray;
  color: white;
}
[theme='cafe'] {
  background: #c0acac;
  color: black;
}
</style>