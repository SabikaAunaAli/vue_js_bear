<template>
  <div class=" bg-white  shadow-lg rounded-3xl p-6 ">
    <div class="flex justify-between mb-4">
      <div class="text-2xl font-bold text-blue">
        {{ selectedOption ? selectedOption : 'Performance Metrics' }}
      </div>
      <div class="relative inline-block">
        <button
          @click="toggleDropdown"
          class="relative bg-gradient-to-b from-teal-500 to-teal-900 rounded-full w-6 h-6 flex items-center justify-center"
        >
          <img class="w-3 h-2" alt="Mask group" src="/src/assets/images/mask-group-12.png" />
          <div v-if="isOpen" class="absolute right-0 top-8 bg-white shadow-lg rounded-xl w-80">
            <a
              v-for="option in options"
              :key="option"
              @click="selectOption(option)"
              class="block text-center text-gradient font-bold py-4 text-lg cursor-pointer hover:shadow-2xl hover:rounded-2xl"
            >
              {{ option }}
            </a>
          </div>
        </button>
      </div>
    </div>

    <!-- Default Performance Metrics Div -->
    <div v-if="!selectedOption" class="space-y-4">
      <div>
        <div class="text-lg font-bold text-blue">Month Performance Percentage:</div>

        <div class="text-base text-blue">43.24%, Ups 37</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Closing Percentage:</div>
        <div class="text-base text-blue">43.24%, Ups 37</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Store Average (closing Percentage):</div>
        <div class="text-base text-blue">67.99%, Ups 50</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Average Sale:</div>
        <div class="text-base text-blue">$3,702.83</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Store Average (average Sale):</div>
        <div class="text-base text-blue">$4,125.84</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Ups Taken For Mtd:</div>
        <div class="text-base text-blue">$4,125.84 June 12</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Store Average (ups Taken For Mtd):</div>
        <div class="text-base text-blue">$4,125.84 June 12</div>
      </div>
      <div>
        <div class="text-lg font-bold text-blue">Performance Index</div>
        <img
          class="w-20 h-6 mb-4"
          alt="Image removebg"
          src="/src/assets/images/image-removebg-preview-3-1.png"
        />
      </div>
    </div>

    <!-- Month Div -->
    <div v-else-if="selectedOption === 'Month'" class="space-y-7">
      <div>
        <div class="text-lg font-bold text-blue">Closing Percentage:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">43.24%</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">67.99%</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >+36.39%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">UPS Taken:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">37</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">50</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >-26.90%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">Average Sale:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">$3,702.83</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">$3,44275</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >+7.56%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">Performance Index:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">1601,22</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">255.134</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >+37.24%</span
            >
          </div>
        </div>
      </div>
    </div>

    <!-- Year Div -->
    <div v-else class="space-y-4">
      <div>
        <div class="text-lg font-bold text-blue">Closing Percentage:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">43.24%</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">37.33%</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >+15.83%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">UPS Taken:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">478</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">550</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >-13.90%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">Average Sale:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">$3,752.44</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">$4,125.84</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >-9.05%</span
            >
          </div>
        </div>
      </div>

      <div>
        <div class="text-lg font-bold text-blue">Performance Index:</div>
        <div class="text-base font-semibold text-blue">
          Salesperson: <span class="font-normal">1601,22</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Store Average: <span class="font-normal">1505.66</span>
        </div>
        <div class="text-base font-semibold text-blue">
          Percentage Difference Displayed As A Circular Graph:
        </div>
        <div>
          <div class="w-fit relative">
            <img class="" alt="Image removebg" src="/src/assets/images/monthly-div.png" />
            <span class="absolute top-7 left-5 text-[9px] font-extrabold text-[#00555D]"
              >+6.35%</span
            >
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
      options: ['Month', 'Year To Date'],
      selectedOption: ''
    }
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen
    },
    selectOption(option) {
      this.selectedOption = option
      this.isOpen = true
    }
  }
}
</script>

<style scoped>
/* Scoped styles can be used for any additional custom styling if needed */

.text-gradient {
  background: linear-gradient(90deg, #00a0af 20%, #00555d 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
