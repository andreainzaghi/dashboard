<template>

    
      <div style="" id="containerprincipe">
       
        <div  id="form" style="margin-bottom:100px;">
            <input type="text" placeholder="E-Mail *" v-model="messageui" value="ciro@gmsil" style="width:87.4%;">
            <input type="password" value=""  v-model="messageui1" placeholder="Password *">
            <input type="password"  value=""  v-model="messageui2" placeholder="Conferma Password *">
            <input type="text"  value=""  v-model="messageui3" placeholder="Nome *">
            <input type="text"  value=""  v-model="messageui4" placeholder="Cognome *">
            <input type="text"  value=""  v-model="messageui5" placeholder="Codice amico" style="width:87.4%;"> 
        </div>
         <div id="form1">
                <input type="checkbox" v-model="check"><span style="">Dati investitore</span>
         </div>
          <div v-if="check" id="form" style="margin:20px 0 100px 0;">
            <input type="text" placeholder="Telefono investitore privato **" v-model="message" value="" >
            <input type="text"  value="" placeholder="Data di nascita investitore privato **">
            <input type="text"  value="" placeholder="Nazionalità investitore privato **">
            <input type="text"  value="" placeholder="Codice Fiscale investitore privato **">
            <input type="text"  value="" placeholder="Provincia di nascita *">
            <input type="text"  value="" placeholder="Comune di nascita *" >
        </div>
          <div id="form2">
              <div>
                <input type="checkbox" ><span style="">Ho letto e compreso il contratto di servizi per investitore, al quale dichiaro di aderire</span>
             </div>
             <div>
                <input type="checkbox" ><span style="">Ho preso visione ed accetto le Condizioni e Termini generali di Lemon Way</span>
             </div>
             <div>
                <input type="checkbox" ><span style="">Ho preso visione dell'Informativa sul trattamento dei dati personali (Finalità a - b)</span>
            </div>
         </div>
         <div style="width:100%;"> 
             <button  style="width:88%;margin-left: 6%;height:50px;margin-top:50px;background-color:blue;color:#fff;border-radius:50px;border:2px solid #fff;">CAMBIA IMPOSTAZIONI</button>
         </div>
  </div>
</template>
<script>
export default {
 
  data () {
    return {
      check: false,
      messageui: 'cirotartaglia@gmail.com',
      messageui1:'messagsdfsfeui1',
      messageui2:'messagsdfsfeui1',
      messageui3:'Ciro',
      messageui4:'Tartaglia'
    }
  },
   methods:{

    }
}
</script>


<style scoped>
#form1 input{
  width:50px;
  margin:10px 20px 0 5% ;
  height:50px;
  background-color: #fff;
  padding:5px 10px;
  border-radius:60px;
  border:1px solid rgb(85, 85, 85);
}
#form2 input{
  width:50px;
  margin:10px 20px 0 5% ;
  height:50px;
  background-color: #fff;
  padding:5px 10px;
  border-radius:60px;
  border:1px solid rgb(85, 85, 85);
  
}
#form2 div{
 display:block;
}

#linky{
 color:rgb(0, 0, 0);
  text-decoration: none;
  border:2px solid rgb(255, 255, 255);
  padding:5px 17px;border-radius:20px;
}
#ddffgg{
  padding:20px;
 
  height:200px;
  width:30%;
  
}
#containerprincipe{
  /* height:650px; */
  /* height:150px; */
 width:100%;
 position:relative;
 background-color:#e2e2e2;
 padding:20px 30px;
 border-radius:10px;
 
  animation: myfirst 1s linear 0.5s infinite alternate;
  background-image:url('/img/dot2.png');
  background-position-x:210px;

  background-size: 930px;
}

@keyframes myfirst {
  0%   {border:1px solid rgb(0, 0, 0);}
 
  100% {border:1px solid rgb(255, 255, 255);}
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
  width:85px;
  height:6px;
  background-color:rgb(0, 0, 0);
  border:2px solid rgb(255, 255, 255);
  transition: 3s;
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
}
button{
  color:black;
}
</style>

