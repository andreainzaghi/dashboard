<template>
  <div>
    <div>
      <h3>COMPLETA  LA TUA REGISTRAZIONE</h3>
      <p style="margin:15px 0;">Per abilitare le funzioni di investimento e poter ricevere il denaro è necessario completare la tua iscrizione inserendo informazioni aggiuntive. Premi l'icona "?" per visualizzare i dati ed i documenti necessari per completare la registrazione.</p>
      <div style="border:1px solid black;width:100%;height:400px;position:relative;background-color:#8EDCF4;padding:10px 20px;">
         <div v-if="errormess" style="text-align:center;color:red;font-weight:bold;">Compila tutti i campi !</div>
        <div v-if="openform" id="form">
            <input type="text" placeholder="Nome *" v-model="message" value="">
            <input type="text" v-model="message1" value="" placeholder="Cognome *">
            <input type="text" v-model="message2" value="" placeholder="Eta' *">
            <input type="text" v-model="message3" value="" placeholder="Telefono *">
            <input type="text" v-model="message4" value="" placeholder="Nazionalita'">
            <input type="text" v-model="message5" value="" placeholder="Codice Fiscale *">
            <input type="text" v-model="message6" value="" placeholder="Citta' *">
            <input type="text" v-model="message7" value="" placeholder="Indirizzo *">
            <button @click="click()" style="width:340px;margin-left:calc(50% - 170px);border:1px solid black;">COMPILA TUTTI I FORM E CLICCA QUI</button>
            
        </div>
        
        <div style="padding:10px 20px;position:absolute;bottom:0;right:0;left:0;">
          <div id="lineafollow"></div>
          <ul style="display:flex;justify-content:space-between;" class="cost-casa">
            <li><button>ABILITATO</button></li>
            <li><button @click="dateRangeText()">ATTIVA ORA</button></li>
            <li><button>COMPLETA</button></li>
           
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
#lineafollow{
  width:10px;
  height:8px;
  background-color:#fff;
  border:1px solid red;
}
#form input{
  width:calc(40% - 20px);
  margin:10px 5%;
  height:50px;
  background-color: #fff;
  padding:5px 10px;
  border-radius:10px;
  border:1px solid black;
}
button{
  color:black;
}
</style>
<script>
export default {
  data () {
    return {
      openform: false,
      message: null,
       message1: null,
        message2: null,
         message3: null,
          message4: null,
           message5: null,
            message6: null,
             message7: null,
             errormess:false
             
     
    }
  },
   methods:{
     dateRangeText() {
       this.openform=true
       
     
               
     },
     click(){
       if(this.message && this.message1 && this.message2 && this.message3 && this.message4 && this.message5 && this.message6 && this.message7){
          this.openform=false
          this.errormess= false 
          const linea = document.querySelector('#lineafollow')
          linea.style.width='50%';
       }else{
        this.errormess= true   
       }
     }
    }
}
</script>
