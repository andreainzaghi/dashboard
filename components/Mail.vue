<template>
    <div>
        <div v-if="openform == true" style="width:340px;height:500px;border:1px solid lightgrey;background-color:#fff;border-radius:10px;padding:15px;position:fixed;bottom:100px;right:40px;z-index:22;">
            <div id="exitid" @click="OpenMail1()" style="position:absolute;top:15px;right:15px;border-radius:20px;padding:1px 7px;border:1px solid grey;">EXIT</div>
            <div >
                <img src="img/logo-recrowd.svg" alt="" style="height:40px;">
                <div>
                   <h3>Assistenza</h3> 
                   <h5>Offline icon Offline</h5>
                </div>
                <div style="width:100%;border:1px solid lightgrey;"> </div>
        
                <div style="overflow:scroll;width:100%;height:325px;padding:1px;padding:0 10px;" id="chatbg">

                  <div  v-for="element in message"  :key="element.id" >
                    <div v-if="element.status == 'sent'"  id="backmessage">
                        <p >{{element.message}}</p>
                        <p><small>{{element.date}}</small></p>
                    </div>
                      <div id="backmessage1" v-else >
                        <p>{{element.message}}</p>
                        <p><small>{{element.date}}</small></p>
                    </div>     
                </div> 

              </div>
                 <div style="width:calc(100% - 30px);border:1px solid lightgrey;margin-top:10px;position:absolute;bottom:15px;right:15px;left:15px;padding:10px;background-color:lightgrey;">
                  
                     <div style="display:flex;align-items:center;"  @keyup.enter="SendMessage()">
                         <input v-model="messagemail"  type="text" style="background-color:#fff;width:100%; border-bottom-left-radius:50px; border-top-left-radius:50px;font-size:12px;padding:10px;border:none;outline:none;border:1px solid grey;" placeholder="In che modo possiamo esserti utili?">
                         <div @click="SendMessage()" style="cursor:pointer; border-bottom-right-radius:50%; background-color:#22AB6E;color:#fff; border-top-right-radius:50%;font-size:12px;padding:10px;border:none;outline:none;border-right:1px solid grey;border-top:1px solid grey;border-bottom:1px solid grey;">SEND</div>
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
#chatbg{
    background-image:url('/img/nuvo.jpg');
  background-position-x:0px;
  background-size: 320px;
}

#exitid:hover{
    background:#F48A39;
    color:#fff;

}
/* width */
::-webkit-scrollbar {
  width: 0px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 0px grey; 
  border-radius: 0px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: red; 
  border-radius: 0px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #b30000; 
}

</style>

<script>
export default {
 
  data () {
    return {
      openform: false,
      finish:false   ,
      sendmess:false   ,
      messaggiovar:null,
      // PROGRAMMATO DA ANDREA INZAGHI
       currentUser:0,
     
         message:[ {
                    date: '10/01/2020 15:50:00',
                    message: 'Ciao, solo per oggi ti chiediamo di lasciarci un messaggio e il nostro team ti contatterà prima possibile.Grazie.',
                    status: 'sent'
                },
          ]
    }
  },
   methods:{
     SendMessage(){
           var dayjs = require('dayjs')
           if (this.messagemail !== ''){
           this.message.push({
              date: dayjs().format('DD/MM/YY HH.MM'),
              message: this.messagemail,
              status: 'sent1'
            });
           this.messagemail = '';
    }
     },
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
#backmessage{
  border:1px solid rgba(188, 188, 188, 0.758);
  padding:10px;margin-top:5px;width:75%;border-radius:10px;font-size:12.5px;
   animation: myfirst2 9s linear 0.1s infinite alternate; font-weight:bold;color:black;
}
#backmessage1{
  border:1px solid rgba(168, 168, 168, 0.758);
  padding:10px;margin-top:5px;width:75%;border-radius:10px;font-size:12.5px;
   animation: myfirst2 9s linear 0.1s infinite alternate; font-weight:bold;color:black;margin-left:25%;
}
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
  0%   {background-color:rgba(255, 141, 11, 0.703);}
  33%  {background-color:#22ab6da7;}
  67%  {background-color:#8edcf494;}
  100% {background-color:rgba(186, 186, 186, 0.607);}
} 
</style> 