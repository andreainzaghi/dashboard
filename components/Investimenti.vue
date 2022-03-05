<template>
<div style="width:100%;">
<h2>INVESTIMENTI</h2>
    <div style="display:flex;width:100%;justify-content:space-around;align-items:center;" >
        
        <div id="inv">
            <div><h3>PROGETTI</h3></div>
            <div><p>0 Finanziamenti</p>
             <p>0 Chiusi</p></div>

        </div>
         <div id="inv">
            <div><h3>RENDIMENTO MEDIO</h3></div>
            <div><p>0.00 %</p><p>Rendimento medio dei tuoi investimenti</p></div>
            

        </div>
    </div>
    <div style="background-color:#E2E2E2;padding:30px;border-radius:10px;margin-top:20px;">
        <p> Ricorda: per ridurre al minimo il rischio è bene diversificare i tuoi investimenti</p>
    </div>
    </div>
</template>
<style scoped>
#inv div{
    color:#fff;
    text-shadow:1px 1px 1px grey;
}
#inv:nth-child(1) {
    padding:20px;
    width:48%;
    margin:1% 1% 0 0;
    border-radius:10px;
    height:150px;
    background-color:#8EDCF4;
      background-image:url('/img/home.png');
  background-position-x:270px;
  background-position-y:-55px;
  background-size: 430px;
  transition:0.3s;
}
#inv:nth-child(2) {
    padding:20px;
    width:49%;
    margin:1% 1% 0 0;
    border-radius:10px;
    height:150px;
    background-color:#8EDCF4;
      background-image:url('/img/trhg.png');
  background-position-x:270px;
  background-position-y:-55px;
  background-size: 430px;
   transition:0.3s;
}
#inv:nth-child(1):hover {
transform: scale(1.02);
}
#inv:nth-child(2):hover {
transform: scale(1.02);
}
</style>