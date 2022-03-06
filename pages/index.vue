<template>
  <div>
    <div>
      <h3>COMPLETA  LA TUA REGISTRAZIONE</h3>
      <p style="margin:15px 0;">Per abilitare le funzioni di investimento e poter ricevere il denaro è necessario completare la tua iscrizione inserendo informazioni aggiuntive. Premi <b @click="dateRangeText()" style="cursor:pointer;">ATTIVA ORA</b>  per visualizzare i dati ed i documenti necessari per completare la registrazione.</p>
      <div style="" id="containerprincipe">
         <div v-if="errormess" style="text-align:center;color:#F48939;font-weight:bold;text-shadow:1px 1px 1px red;">PERFAVORE COMPILA TUTTI I CAMPI !</div>
        <div v-if="openform" id="form" style="margin-bottom:100px;background-image:url('/img/dots1.png');   background-size: cover;">
            <input type="text" placeholder="Nome *" v-model="message" value="">
            <input type="text" v-model="message1" value="" placeholder="Cognome *">
            <input type="text" v-model="message2" value="" placeholder="Eta' *">
            <input type="text" v-model="message3" value="" placeholder="Telefono *">
            <input type="text" v-model="message4" value="" placeholder="Nazionalita'">
            <input type="text" v-model="message5" value="" placeholder="Codice Fiscale *">
            <input type="text" v-model="message6" value="" placeholder="Citta' *">
            <input type="text" v-model="message7" value="" placeholder="Indirizzo *">
            <button @click="click()" id ="btn-formi" style="width:340px;margin-left:calc(50% - 170px);padding:10px;border-radius:5px;margin-top:10px;">COMPILA TUTTI I FORM E CLICCA QUI</button>
            
        </div>
        <div v-if="!first" style="display:flex;width:100%;justify-content:center;align-items:center;font-weight:bold;">
          <p style="color:#fff;display:flex;width:100%;justify-content:center;align-items:center;text-shadow:1px 1px 1px black;" >Inizia la tua esperienza con <img src="img/logo-recrowd.svg" alt="" style="height:30px;margin:0 15px;"><b @click="dateRangeText()" style="cursor:pointer;"> CLICCA su ATTIVA ORA</b>
         </p>
        </div>
         <div v-if="second" style="display:flex;width:100%;justify-content:center;align-items:center;font-weight:bold;">
            <div v-if="!openform" style="position:absolute;top:10px;left:10px;">
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">REPEAT :</div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Nome : <b>{{message}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Cognome :<b>{{message1}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Eta' :<b>{{message2}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Telefono :<b>{{message3}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Nazionalita' :<b>{{message4}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Codice Fiscale :<b>{{message5}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Citta' :<b>{{message6}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;">Indirizzo :<b>{{message7}}</b></div>
              <div style=" color:grey;text-shadow:1px 1px 1px #fff;"><button @click="dateRangeText()" id="linky">MODIFICA DATI :</button></div>
          </div>
        <div class="payment">
         
              <div class="bg"></div>
              <div class="card">
                <img src="img/chip.png" class="chip">
                <div class="logo"></div>
                <h2 class="bankName" contenteditable="true"> </h2>
                <form>
                  <div class="inputBox">
                    <span>Card N°</span>
                    <input type="text" placeholder="0123 4567 8901 2345" maxlength="19">
                  </div>
                  <div class="inputBox">
                    <span>Card Holder</span>
                    <input type="text" :placeholder="message">
                  </div>
                  <div class="group">
                    <div class="inputBox">
                      <span>Valid Thru</span>
                      <input type="text" placeholder="MM/YY" maxlength="5">
                    </div>
                    <div class="inputBox">
                      <span>CCV</span>
                      <input type="password" placeholder="***" maxlength="4">
                    </div>
                  </div>
                </form>
              </div>
              <button class="btn" @click="completa()">COMPLETA</button>
              
            </div>
        </div>
      
        
        <div style="padding:10px 20px;position:absolute;bottom:0;right:0;left:0;">
          <div id="lineafollow"></div>
          <ul style="display:flex;justify-content:space-between;" class="cost-casa">
            <li><button > ABILITATO -></button></li>
            <li><button @click="dateRangeText()" id="linky">ATTIVA ORA</button></li>
            
           
          </ul>
        </div>
      </div>
        <div v-if="finish">
           <h1 style="color:#22AB6E;">TRANSAZIONE COMPLETATA!</h1>
        </div>
    </div>
    <div style="margin-top:20px;">
      <div>
        <h1>Ciao, Ciro Tartaglia</h1>
      </div>
    
    </div>
    <SecondNavbar/>
  </div>
</template>
<style scoped>
div b{
  color:#000000;
  text-shadow: 1px 1px rgb(255, 255, 255);
}
#btn-formi{
border:1px solid grey;
}
#btn-formi:hover{
background-color: #F48939;
border:1px solid #ffffff;
color:#fff;
}
#linky{
 color:rgb(0, 0, 0);
  text-decoration: none;
  border:2px solid rgb(255, 255, 255);
  padding:5px 17px;border-radius:20px;
    animation: myfirst1 2s linear 0.5s infinite alternate;
}
#ddffgg{
  padding:20px;
 
  height:200px;
  width:30%;
  
}
#containerprincipe{
  /* height:650px; */
  /* height:150px; */
 width:100%;position:relative;background-color:#e2e2e2;padding:20px 30px;border-radius:10px;
 
  animation: myfirst 1s linear 0.5s infinite alternate;
   
}
@keyframes myfirst {
  0%   {border:1px solid rgb(255, 255, 255);}
 
  100% {border:1px solid rgb(255, 141, 11);}
}
@keyframes myfirst1 {
  0%   {border:2px solid rgb(255, 255, 255);}
 
  100% {border:2px solid rgb(255, 141, 11);}
}
.payment
{
	position: relative;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	padding: 0px;
	transform: translateY(-63px);
	transition: 0.5s;
}
.payment:hover
{
	padding: 40px;
	transform: translateY(0);
}
.payment .bg
{
	position: absolute;
	bottom: 0;
	height: 70%;
	width: 100%;
	border-radius: 25px;
	background: linear-gradient(225deg,#ea222cc3,#FED090);
}
.payment .card
{
	position: relative;
	width: 580px;
	height: 350px;
	background: #fcfcfc;
	border-radius: 15px;
	padding: 40px;
	box-shadow: 6px 6px 12px rgba(0,0,0,0.05);
	z-index: 1000;
	overflow: hidden;
	transform: translateY(127px);
	transition: 0.5s;
}
.payment:hover .card
{
	transform: translateY(0);
}
.payment .card::before
{
	content: '';
	position: absolute;
	top: -50%;
	left: -20%;
	width: 500px;
	height: 500px;
	border-radius: 50%;
	background: linear-gradient(to bottom,rgba(0,0,0,0.05),transparent);
	pointer-events: none;
}
.chip
{
	position: absolute;
	max-width: 70px;
}
.logo
{
	position: absolute;
	top: 130px;
	right: 40px;
	width: 60px;
	height: 60px;
	background: #ea222c;
	border-radius: 50%;
	box-shadow: -40px 0 0 rgba(255,164,36,0.5);
}
.bankName
{
	color: #999;
	text-align: end;
	outline: none;
	width: 100%;
	font-size: 1.5em;
}
form
{
	margin-top: 45px;
}
.inputBox
{
	display: flex;
	flex-direction: column;
	margin-bottom: 20px;
}
.inputBox span
{
	color: #089cff;
	font-size: 1.1em;
}
.inputBox input 
{
	border: none;
	outline: none;
	background: transparent;
	font-size: 1.8em;
	color: #333;
	font-family: 'Share Tech Mono', monospace;
}
.group
{
	width: 100%;
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.group .inputBox:last-child
{
	max-width: 60px;
}
.btn
{
	position: relative;
	margin-top: 40px;
	padding: 15px 20px;
	border-radius: 5px;
	border: none;
	outline: none;
	background: #fff;
	color: #333;
	font-size: 1.5em;
	cursor: pointer;
	box-shadow: 3px 3px 6px rgba(0,0,0,0.1);
}
#lineafollow{
  width:83px;
  height:6px;
  background-color:rgb(229, 134, 11);
  border:2px solid rgb(255, 255, 255);
  transition: 3.5s;
  border-radius: 5px;
}
#form input{
  width:calc(40% - 20px);
  margin:10px 5%;
  height:50px;
  background-color: #fff;
  padding:5px 10px;
  border-radius:60px;
  border:1px solid rgb(85, 85, 85);
  outline:none;
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
             errormess:false,
             first:false,
             second:false,
             finish:false
             
     
    }
  },
   methods:{
     dateRangeText() {
       this.openform=true;
        this.first=true;
        const linea1 = document.querySelector('#containerprincipe')
          linea1.style.height='450px';
               
     },
      completa() {
      this.finish=true;
        const linea1 = document.querySelector('#containerprincipe')
          linea1.style.display='none';
               
     },
     click(){
        const linea1 = document.querySelector('#containerprincipe')
          linea1.style.height='650px';
           
       if(this.message && this.message1 && this.message2 && this.message3 && this.message4 && this.message5 && this.message6 && this.message7){
          this.openform=false
          this.errormess= false 
          const linea = document.querySelector('#lineafollow')
          linea.style.width='100%';
           this.second=true;
       }else{
        this.errormess= true   
       }
     }
    }
}
</script>
