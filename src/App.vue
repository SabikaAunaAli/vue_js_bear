<script setup>
import OpenAndScheduled from "./components/OpenAndScheduled.vue";
import MattressMetrics from "./components/MattressMetrics.vue";
import PerformanceMetrics from "./components/PerformanceMetrics.vue";
import UnitersMetrics from "./components/UnitersMetrics.vue";
import GersReports from "./components/GersReports.vue";
import SideBar from "./components/SideBar.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import UpcomingOrders from "./components/UpcomingOrders.vue";
import AllEmail from "./components/AllEmail.vue";
</script>

<template>
  <div class="flex space-y-4 ">
    <div >
      <SideBar />
    </div>

    <div class="">
      <div class=" ">
        <Header />
      <div class="grid grid-cols-3 gap-4  ">   
    <div class="col-span-2">
      <div class="grid grid-cols-2 gap-4">
      <div class="flex-col space-y-4 ml-4 ">
      <OpenAndScheduled />
      <MattressMetrics />
    </div>
    <div class="flex-col space-y-4 ">
      <PerformanceMetrics />
      <UnitersMetrics />
    </div>

    </div>
    <div>
      <GersReports />
    </div>

    </div>

    <div class=" mr-4 ">
      <UpcomingOrders/>
      <div class="mt-6">
        <AllEmail/>

      </div>
   

    </div>
    <div class="col-span-3">
      <Footer/>
    </div>
    
  </div>
    

   
  </div>
</div>



</div>


</template>
