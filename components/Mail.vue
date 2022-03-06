<template>
    <div>
        <div id="mail">
                    <img src="img/mails.png" alt="" style="width:60px;">
        </div>
    </div>
</template>
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
  0%   {background-color:orange;border-top-left-radius: 50%;}
  33%   {background-color:rgb(76, 251, 63);border-top-right-radius: 50%;}
   67%   {background-color:rgb(0, 221, 255);border-bottom-left-radius: 50%;}
  100% {background-color: rgb(186, 186, 186);border-bottom-right-radius: 50%;}
} 
</style>