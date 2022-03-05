<template>
<div style="width:100%;">
<h2>IL TUO CONTO VIRTUALE</h2>
    <div style="display:flex;width:100%;justify-content:space-around;align-items:center;" >
        
        <div id="inv" @click="ContoVirtuale1()" >
            <div>
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"  viewBox="0 0 50 50" version="1.1" class="svg card-title replaced-svg">
                    <!-- Generator: Sketch 55.2 (78181) - https://sketchapp.com -->
                    <title>icon-add</title>
                    <desc>Created with Sketch.</desc>
                    <g id="icon-add" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="add-button-inside-black-circle" transform="translate(5.000000, 5.000000)" fill="#ffffff" fill-rule="nonzero">
                            <path d="M20,0 C9,0 0,9 0,20 C0,31 9,40 20,40 C31,40 40,31 40,20 C40,9 31,0 20,0 Z M30,22 L22,22 L22,30 L18,30 L18,22 L10,22 L10,18 L18,18 L18,10 L22,10 L22,18 L30,18 L30,22 Z" id="Shape"></path>
                        </g>
                        <path d="M25.0033784,0 C11.1991892,0 0.00716216216,11.1924324 0.00716216216,24.997027 C0.00716216216,38.8006757 11.1991892,49.9932432 25.0033784,49.9932432 C38.8078378,49.9932432 49.9995946,38.8008108 49.9995946,24.997027 C49.9995946,11.1924324 38.8078378,0 25.0033784,0 Z M25.0033784,47.7722973 C12.4436486,47.7722973 2.22824324,37.5543243 2.22824324,24.997027 C2.22824324,12.4389189 12.4436486,2.22175676 25.0033784,2.22175676 C37.5616216,2.22175676 47.7777027,12.4387838 47.7777027,24.997027 C47.7777027,37.5541892 37.5614865,47.7722973 25.0033784,47.7722973 Z" id="Shape" fill="#ffffff" fill-rule="nonzero"></path>
                    </g>
                </svg>
            </div>
            <div><h3>AGGIUNGI FONDI</h3>
             <p>Tramite Carta di Credito o Bonifico</p></div>

        </div>
         <div id="inv" @click="ContoVirtuale1()" >
            <div>
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"  viewBox="0 0 50 50" version="1.1" class="svg card-title replaced-svg">
                    <!-- Generator: Sketch 55.2 (78181) - https://sketchapp.com -->
                    <title>icon-cash-out</title>
                    <desc>Created with Sketch.</desc>
                    <g id="icon-cash-out" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="download-archive-tray" fill="#ffffff" fill-rule="nonzero">
                            <g id="add-button-inside-black-circle" transform="translate(5.000000, 5.000000)">
                                <path d="M20,0 C31,0 40,9 40,20 C40,31 31,40 20,40 C9,40 0,31 0,20 C0,9 9,0 20,0 Z M20.0457456,26.499693 L28.0457456,18.3178895 L23.2457561,18.3178895 L23.2457561,8.49969298 L16.8457351,8.49969298 L16.8745251,18.3178895 L12.0457456,18.3178895 L20.0457456,26.499693 Z M26.7124123,26.499693 L26.7124123,29.499693 L13.3790789,29.499693 L13.3790789,26.499693 L10.0457456,26.499693 L10.0457456,29.499693 L10.0457456,32.499693 L30.0457456,32.499693 L30.0457456,26.499693 L26.7124123,26.499693 Z" id="Shape"></path>
                            </g>
                            <path d="M25.0033784,0 C11.1991892,0 0.00716216216,11.1924324 0.00716216216,24.997027 C0.00716216216,38.8006757 11.1991892,49.9932432 25.0033784,49.9932432 C38.8078378,49.9932432 49.9995946,38.8008108 49.9995946,24.997027 C49.9995946,11.1924324 38.8078378,0 25.0033784,0 Z M25.0033784,47.7722973 C12.4436486,47.7722973 2.22824324,37.5543243 2.22824324,24.997027 C2.22824324,12.4389189 12.4436486,2.22175676 25.0033784,2.22175676 C37.5616216,2.22175676 47.7777027,12.4387838 47.7777027,24.997027 C47.7777027,37.5541892 37.5614865,47.7722973 25.0033784,47.7722973 Z" id="Shape"></path>
                        </g>
                    </g>
                </svg>
            </div>
            <div><h3>RITIRA CASH-OUT</h3><p>Hai del credito da ritirare</p></div>
            

        </div>
    </div>
    <div style="background-color:#E2E2E2;padding:30px;border-radius:10px;margin-top:20px;">
        <p> Ultimi Movimenti</p>
    </div>
    <div v-if="openform" style="background-color:#E2E2E2;padding:30px;border-radius:10px;margin-top:20px;border:2px dashed  grey;">
       
         <div style="display:flex;justify-content:space-between;align.items:center;">
              <div>CONTO VIRTUALE CLIENTE NON ABILITATO</div>
              <div @click="ContoVirtuale2()" style="width:55px;border:1px solid grey;padding:10px;">EXIT</div>
          </div>
          <div>
              Per poter abilitare il tuo conto virtuale è necessario caricare il documento d’identità tramite la tua Dashboard
          </div>
           <div @click="ContoVirtuale2()" style="width:90px;border:1px solid grey;padding:10px;">ANNULLA</div>
    </div>
    
    </div>
</template>
<script>
export default {
 
  data () {
    return {
      openform: false,
    
 
             
     
    }
  },
   methods:{
   
     ContoVirtuale1(){
       this.openform=true;
       
       
     },
      ContoVirtuale2(){
      
        this.openform=false;
        
       
     },
   
    }
}
</script>
<style scoped>
#inv div{
    color:#fff;
    text-shadow:1px 1px 1px rgb(32, 32, 32);
}
svg{
    width:60px;
}
#inv:nth-child(1) {
    padding:20px;
    width:48%;
    margin:1% 1% 0 0;
    border-radius:10px;
    height:150px;
    background-color:#dbdbdb;
      background-image:url('/img/credit.png');
  background-position-x:270px;
  background-position-y:-55px;
  background-size: 430px;
  transition:0.3s;
  border:2px dashed  grey;
}
#inv:nth-child(2) {
    padding:20px;
    width:49%;
    margin:1% 1% 0 0;
    border-radius:10px;
    height:150px;
    background-color:#eaeaea;
      background-image:url('/img/gpig.png');
  background-position-x:300px;
  background-position-y:-30px;
  background-size: 230px;
   transition:0.3s;
   border:2px dashed  grey;
}
#inv:nth-child(1):hover {
transform: scale(1.02);
}
#inv:nth-child(2):hover {
transform: scale(1.02);
}
</style>