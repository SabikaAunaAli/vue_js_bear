<template>
  <div class="flex m-4 justify-between  p-4">
    <div class=" flex-col items-center">
      <div class="text-4xl text-blue font-bold">Hi, BAER`S</div>
      <p class="text-base font-normal">Let`s Check Your Store Today</p>
    </div>

    <div class="relative flex items-center">
      <img
        class="absolute left-3 inline h-5 w-5"
        alt="Mask group"
        src="/src/assets/images/search.png"
      />
      <input
        type="search"
        placeholder="Search..."
        class="text-lg pl-12 py-2 pr-4  w-[580px] border rounded-full shadow-2xl focus:outline-none focus:ring-2 focus:ring-teal-700"
      />
    </div>


    <div class="flex items-center ">
<!-- Icon Section -->
<div class="flex items-center space-x-4 mr-5">
    <div class="relative">
      <img class="w-6 h-6" alt="Mail" src="/src/assets/images/mail.png" />
      <div class="absolute top-0 right-0 w-3 h-3 bg-yellow-400 border-[1px] border-black rounded-full"></div>
    </div>
 
    <div class="relative">
      <img class="w-6 h-6" alt="Mail" src="/src/assets/images/notification.png" />

    </div>
  </div>

  <!-- Image Section -->
  <div class=" mr-2">
    <img class="w-16 rounded-full" alt="Ellipse" src="/src/assets/images/profile.png" />
  </div>

  <!-- Text Section -->
  <div>
    <div class="text-lg font-bold">BAER`S</div>
    <div class="text-sm ">Lorem Ipsum</div>
  </div>

  
</div>



  </div>
</template>
