<template>
    <div>
        <div v-if="openform == true" style="width:300px;height:500px;border:1px solid lightgrey;background-color:#fff;border-radius:10px;padding:15px;position:fixed;bottom:100px;right:40px;z-index:22;">
            <div id="exitid" @click="OpenMail1()" style="position:absolute;top:15px;right:15px;border-radius:20px;padding:1px 7px;border:1px solid grey;">EXIT</div>
            <div>
                <img src="img/logo-recrowd.svg" alt="" style="height:40px;">
                <div>
                   <h3>Assistenza</h3> 
                   <h5>Offline icon Offline</h5>
                </div>
                <div style="width:100%;border:1px solid lightgrey;"> </div>
                 <div style="width:calc(100% - 30px);border:1px solid lightgrey;margin-top:10px;position:absolute;bottom:15px;right:15px;left:15px;padding:10px;background-color:lightgrey;">
                     <div>
                         <input type="text" style="background-color:#fff;width:100%;border-radius:20px;font-size:12px;padding:10px;border:none;outline:none;border:1px solid grey;" placeholder="In che modo possiamo esserti utili?">
                     </div>
                 </div>
            </div>
        </div>
        <div id="mail" @click="OpenMail()">
               <img src="img/mails.png" alt="" style="width:40px;">
        </div>
        
    </div>
</template>
<style scoped>
#exitid:hover{
    background:#F48A39;
    color:#fff;

}

</style>

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
     
               
     },
     OpenMail1() {
       this.openform=false;
        this.first=false;
     
               
     },
 
    },
}
</script>

<style scoped>
#mail{
    height:60px;
    width:60px;
   display:flex;
   justify-content: center;
   align-items:center;
 animation: myfirst2 4s linear 0.1s infinite alternate; 
  border-radius:50%;
  
}
#mail:hover{
    height:60px;
    width:60px;
   display:flex;
   justify-content: center;
   align-items:center;
    border-top-right-radius:1%;
    border-top-left-radius:50%;
   border-bottom-right-radius:50%;
   border-bottom-left-radius:50%;
 
   
}

 @keyframes myfirst2 {
  0%   {background-color:rgb(255, 141, 11);}
  33%  {background-color:#22AB6E;}
  67%  {background-color:#8EDCF4;}
  100% {background-color:rgb(186, 186, 186);}
} 
</style> 