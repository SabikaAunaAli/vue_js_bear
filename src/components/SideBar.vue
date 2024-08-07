<template>
  <div class="flex flex-col bg-white px-8 font-josefin rounded-xl space-y-8  h-full pt-8 ">

     <div class="flex flex-col space-y-2">
      <img class="w-44 h-24 mb-8 " src="../assets/images/image-5-1.png" alt="">
      
       <div class="h-[698px] w-[169px] flex flex-col space-y-8 ">
        <div class="h-[41px] w-full bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-xl py-2 px-2">
        <div class="flex items-center space-x-2 ">
           <img class="h-[18px] w-[18px]" alt="Mask group" src="/src/assets/images/mask-group.png" />
           <div class="text-white text-[16px] font-medium leading-[20px]">Home</div>
         </div>
       </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[22px] w-[20px]" alt="Envelope" src="/src/assets/images/envelope-1.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Baer’s Email</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2 ">
           <img class="h-[22px] w-[18px]" alt="Envelope" src="/src/assets/images/envelope-2.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">White Copy</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[19px] w-[16px]" alt="Vector" src="/src/assets/images/vector.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]"> Statement</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[16px] w-[16px]" alt="Vector" src="/src/assets/images/vector-1.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Elavon</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[18px] w-[18px]" alt="Envelope" src="/src/assets/images/envelope-1-1.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Perq</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[18px] w-[18px]" alt="Envelope" src="/src/assets/images/envelope-1-2.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Open Orders</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[16px] w-[16px]" alt="Vector" src="/src/assets/images/vector-2.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Design Links</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[18px] w-[18px]" alt="Envelope" src="/src/assets/images/envelope-1-3.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Vendor Links</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[16px] w-[15px]" alt="Vector" src="/src/assets/images/vector-3.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Shipping</div>
         </div>
         <div class="flex items-center space-x-2 bg-hover px-2">
           <img class="h-[16px] w-[13px]" alt="Vector" src="/src/assets/images/vector-4.svg" />
           <div class="text-[#00555d] text-[16px] leading-[20px]">Mattress Report</div>
         </div>
       </div>
     </div>
   </div>
 </template>
 
 <script>
 export default {
   name: 'Group16'
 }
 </script>
 
 <style>
 @import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@400;500&display=swap');
 
 .font-josefin {
   font-family: 'Josefin Sans', sans-serif;
 }

 .bg-hover:hover {
  background: linear-gradient(90deg, #00A0AF 0%, #00555D 100%);
  /* transition: background-color 0.2s ease-in-out; */
  padding: 8px;
  border-radius: 10px;
  color: white;
  cursor: pointer;
}

.bg-hover:hover div {
    color: white;
  }
 </style>
 