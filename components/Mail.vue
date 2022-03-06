<template>
    <div>
        <div id="mail" @click="OpenMail()">
                    <img src="img/mails.png" alt="" style="width:60px;">
        </div>
        <!-- <div style="width:300px;height:500px;backgroud-color:red;position:fixed;bottom:120px;z-index:22;">
<div>s</div>
        </div> -->
    </div>
</template>

<script>
export default {
 
  data () {
    return {
      openform: false,
      finish:false      
    }
  },
   methods:{
     OpenMail() {
       this.openform=true;
        this.first=true;
        const linea1 = document.querySelector('#containerprincipe')
          linea1.style.height='450px';
               
     },
 
    }
}
</script>

<style scoped>
#mail{
    height:80px;
    width:80px;
   display:flex;
   justify-content: center;
   align-items:center;
  animation: myfirst2 8s linear 0.1s infinite alternate;
   
}

@keyframes myfirst2 {
  0%   {background-color:rgb(255, 141, 11);;border-top-left-radius: 50%;}
  33%   {background-color:#22AB6E;border-top-right-radius: 50%;}
   67%   {background-color:#8EDCF4;border-bottom-left-radius: 50%;}
  100% {background-color: rgb(186, 186, 186);border-bottom-right-radius: 50%;}
} 
</style>