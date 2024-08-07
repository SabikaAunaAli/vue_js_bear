<template>
  <div class=" bg-white rounded-2xl shadow-lg  ">
    <div class="flex items-center justify-between p-8">
      <div class="text-2xl font-bold text-blue">
        <p>Uniters Metrics</p>
      
    

      </div>

      <div class="relative inline-block">
        <button
          @click="toggleDropdown"
          class="relative bg-gradient-to-b from-teal-500 to-teal-900 rounded-full w-6 h-6 flex items-center justify-center"
        >
          <div class="relative">
            <img class="w-3 h-2" alt="Mask group" src="/src/assets/images/mask-group-12.png" />
          </div>
        </button>
        <div
          v-if="isOpen"
          class="absolute right-0 top-8 bg-white w-80 shadow-lg z-10 hover:text-gradient rounded-lg mt-2 hover:shadow-xl"
        >
          <a
            v-for="choice in choices"
            :key="choice"
            @click="selectChoice(choice)"
            class="block text-center text-gradient font-bold py-4 text-lg bg-cyan-300 cursor-pointer hover:shadow-xl hover:rounded-2xl"
          >
            {{ choice }}
          </a>
        </div>
      </div>
    </div>

    <!-- Written Order -->
    <div v-if="selectedChoice === 'Written Order'" class="p-6">
      <div class="flex flex-col ">
        <div class="flex">
          <div
            class="w-28 h-28 -mt-10 bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-8.png" />
          </div>
          <div class="ml-4 flex-1 -mt-5">
            <div class="text-[28px] font-bold text-blue">Written Order</div>
            <div class="space-y-4 mt-4">
              <div class="flex flex-col space-y-2">
                <div class="text-lg font-bold text-blue">Month-to-Date (MTD):</div>
                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Unites For: <span class="font-normal">2,500</span>
                </div>
                </div>
             
              </div>
              <div class="flex flex-col space-y-2">
                <div class="text-lg font-bold text-blue">Year-to-Date (YTD):</div>
                <p class="text-sm text-blue">2023 1 of 22.000 For Unites</p>
              </div>
              <div class="flex flex-col space-y-1">
                <div class="flex items-center space-x-2">
                  <p class="text-base font-bold text-blue">Percentage of Total Sales (MTD):</p>
                </div>
                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Sale So For: <span class="font-normal">$100,000</span>
                </div>
                </div>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-7 text-[9px] font-extrabold text-[#00555D]"
              >2.91%</span
            >
          </div>

              <div class="flex flex-col space-y-1">
                <div class="flex items-center space-x-2">
                  <p class="text-base font-bold text-blue">Percentage Of Total Sales (YTD):</p>
                
                </div>

                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Sales So For: <span class="font-normal">$1,200,000</span>
                </div>
                </div>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-6 text-[10px] font-extrabold text-[#00555D]"
              >2.21%</span
            >
          </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Delivered Order -->
    <div v-if="selectedChoice === 'Delivered Order'" class="p-6">
      <div class="flex flex-col ">
        <div class="flex">
          <div
            class="w-28 h-28 -mt-10 bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-8.png" />
          </div>
          <div class="ml-4 flex-1 -mt-5">
            <div class="text-[28px] font-bold text-blue">Delivered Order</div>
            <div class="space-y-4 mt-4">
              <div class="flex flex-col space-y-2">
                <div class="text-lg font-bold text-blue">Month-to-Date (MTD):</div>
                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Unites For: <span class="font-normal">$3,500</span>
                </div>
                </div>
             
              </div>
              <div class="flex flex-col space-y-2">
                <div class="text-lg font-bold text-blue">Year-to-Date (YTD):</div>
                <p class="text-sm text-blue">2023 1 of 150.000 For Mattress</p>
              </div>
              <div class="flex flex-col space-y-1">
                <div class="flex items-center space-x-2">
                  <p class="text-base font-bold text-blue">Percentage of Total Sales (MTD):</p>
                </div>
                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Sale So For: <span class="font-normal">$120,000</span>
                </div>
                </div>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-7 text-[9px] font-extrabold text-[#00555D]"
              >2.91%</span
            >
          </div>

              <div class="flex flex-col space-y-1">
                <div class="flex items-center space-x-2">
                  <p class="text-base font-bold text-blue">Percentage Of Total Sales (YTD):</p>
                
                </div>

                <div class="flex justify-start space-x-5">
                <div class="text-sm font-semibold text-blue">
                  Date: <span class="font-normal">Jan 1</span>
                </div>

                <div class="text-sm font-semibold text-blue">
                  Sale So For: <span class="font-normal">$140,000</span>
                </div>
                </div>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-6 text-[10px] font-extrabold text-[#00555D]"
              >2.21%</span
            >
          </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      isOpen: false,
      choices: ['Written Order', 'Delivered Order'],
      selectedChoice: 'Written Order'
    }
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen
    },
    selectChoice(choice) {
      this.selectedChoice = choice
      this.isOpen = false
    }
  }
}
</script>

<style scoped>
/* Scoped styles can be used for any additional custom styling if needed */

.text-gradient {
  background: linear-gradient(10deg, #00a0af 10%, #00555d 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
