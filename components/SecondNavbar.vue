<template>
      <div style="display:flex;justify-content:space-between;align-items:center;margin-top:20px;" id="dashchoose">
          <div id="ddffgg">
                <NuxtLink to="/ricaricaoritira" prefetchLinks id="linky">
                    <div><h3>Conto Virtuale</h3></div>
                    <div>0.00$</div>
                    <div><p>Disponibile</p></div>
                </NuxtLink>
          </div>
      

         <div id="ddffgg">
              <NuxtLink to="/ricaricaoritira" prefetchLinks id="linky">
                <div><h3>Investimenti</h3></div>
                <div>0.00$</div>
                <div><p>Investi</p></div>
           </NuxtLink>
          
        </div>

         <div id="ddffgg">
              <NuxtLink to="/ricaricaoritira" prefetchLinks id="linky">
                <div>
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 50 50" version="1.1" class="svg card-title replaced-svg">
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
                <div><h4>Cash-Out</h4></div>
                <div><p>Credito</p></div>
           </NuxtLink>
        </div>
      </div>
</template>


<style scoped>
svg{
    width:60px;
}
#linky{
 color:#fff;
  text-decoration: none;
  text-shadow: 1px 1px 1px grey;;
}
#ddffgg{
  padding:20px;
 
  height:200px;
  width:30%;
  border-radius:10px;
  transition: 0.2s;
}
#ddffgg:hover{
 transform: scale(1.02);
 

}
#ddffgg:first-child{

  background-color:#f48a39;
  background-image:url('/img/pigs.png');
  background-position-x:200px;
  background-position-y:25px;
  background-size: 230px;
}
#ddffgg:nth-child(2){

  background-color:#8EDCF4;
   background-image:url('/img/weed.png');
  background-position-x:190px;
  background-position-y:-10px;
   background-size: 230px;
}
#ddffgg:nth-child(3){

  background-color:#DA3A51;
   background-image:url('/img/moneyrain.png');
  background-position-x:60px;
  background-position-y:5px;
   background-size: 280px;
}
</style>