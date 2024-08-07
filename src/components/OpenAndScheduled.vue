<template>
  <div class="mattress-metrics bg-white rounded-2xl shadow-lg py-2 ">
    <div class="flex items-center justify-end p-8">

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
    <div v-if="selectedChoice === 'Open And Scheduled Orders'" class="p-6">
      <div class="text-2xl font-bold text-blue -mt-20 mb-10">
        <p>Open And Scheduled Orders</p>
      </div>
      <div class="flex flex-col space-y-8 ">
        <div class="flex">
          <div
            class="w-28 h-28  bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-5.png" />
          </div>
          <div class="ml-4 flex-1 ">
            <div class="text-[28px] font-bold text-blue">Open Order Dollar Amount</div>
            <div>
              $ 30.00
            </div>
          </div>
        </div>

        <div class="flex">
          <div
            class="w-28 h-28 -mt-2  bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-3.png" />
          </div>
          <div class="ml-4 flex-1 ">
            <div class="text-[28px] font-bold text-blue">Scheduled Order <br> Dollar</div>
            <div>
              $ 50.000
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Delivered Order -->
    <div v-if="selectedChoice === 'Written And Delivered Orders'" class="p-6">
      <div class="text-2xl font-bold text-blue -mt-20 mb-10">
        <p>Written And Delivered Orders</p>
      </div>
      <div class="flex flex-col space-y-8 ">
        <div class="flex">
          <div
            class="w-28 h-28  bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-8.png" />
          </div>
          <div class="ml-4 flex-1 ">
            <div class="text-[28px] font-bold text-blue">Written Order Dollar Amount</div>
            <div class="space-y-2 mt-4">
              <div class="flex flex-col space-y-2">
              
                <div class="flex justify-between ">
                <div class="text-lg font-bold text-blue">
                  Year: <div class="font-normal">$1,200,00</div>
                </div>

                <div class="text-lg font-bold text-blue ml-10">
                  Dollar Amount Previous  Year: <div class="font-normal">$1,250,000</div>
                </div>
                </div>
             
              </div>
              <div class="flex flex-col">
                <div class="text-lg font-bold text-blue">Changes:</div>
                <p class="font-normal text-blue">$ 50.000</p>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-6 text-[10px] font-extrabold text-[#00555D]"
              >0.4%</span
            >
          </div>

        
            </div>
          </div>
        </div>

        <div class="flex">
          
          <div
            class="w-28 h-28   bg-gradient-to-b from-[#00a0af] to-[#00555d] rounded-full flex items-center justify-center"
          >
            <img class="w-[70px] h-[70px]" alt="Mask group" src="/src/assets/images/mask-group-9.png" />
          </div>
          <div class="ml-4 flex-1 ">
            <div class="text-[28px] font-bold text-blue">Delivered Order Dollar Amount</div>
            <div class="space-y-2 mt-4">
              <div class="flex flex-col space-y-2">
              
                <div class="flex justify-between ">
                <div class="text-lg font-bold text-blue">
                  Year: <div class="font-normal">$1,400,00</div>
                </div>

                <div class="text-lg font-bold text-blue ml-10">
                  Dollar Amount Previous  Year: <div class="font-normal">$1,30,000</div>
                </div>
                </div>
             
              </div>
              <div class="flex flex-col">
                <div class="text-lg font-bold text-blue">Changes:</div>
                <p class="font-normal text-blue">$ 100,000</p>
              </div>
              <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-6 left-5 text-[10px] font-extrabold text-[#00555D]"
              >7.69%</span
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
      choices: ['Open And Scheduled Orders', 'Written And Delivered Orders'],
      selectedChoice: 'Open And Scheduled Orders'
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
