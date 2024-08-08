<template>
  <div class="bg-white px-4 pb-4 shadow-xl rounded-3xl">
    <div class="flex align-middle items-center justify-between">
      <div class="m-5 py-2 text-[#00555D] font-bold text-2xl">
        Upcoming Orders
      </div>

      <div>
    <!-- Current week -->
    <div v-if="showCurrentWeek" class="flex items-center justify-center space-x-3 ml-11">
      <div
        class="text-white font-bold relative bg-gradient-to-b from-teal-500 to-teal-900 rounded-full py-2 px-4 text-nowrap"
      >
        Current week
      </div>
      <div class="rounded-full overflow-hidden shadow-xl">
        <img 
          class="cursor-pointer" 
          alt="Next week" 
          src="/src/assets/images/arrow.png" 
          @click="toggleWeek"
        />
      </div>
    </div>

    <!-- Next week -->
    <div v-if="!showCurrentWeek" class="flex items-center justify-center space-x-3 ml-11">
      <div class="rounded-full overflow-hidden shadow-xl">
        <img 
          class="rotate-180 cursor-pointer" 
          alt="Current week" 
          src="/src/assets/images/arrow.png" 
          @click="toggleWeek"
        />
      </div>
      <div class="text-white font-bold relative bg-gradient-to-b from-teal-500 to-teal-900 rounded-full py-2 px-4 text-nowrap">
        Next week
      </div>
    </div>
  </div>


    </div>

    <!-- first Table -->

    <div class="w-full max-w-4xl rounded-xl border border-[#D9D9D9] p-2">
      <table class="w-full table-auto">
        <tbody>
          <tr>
            <td
              class="w-3/4 px-4 py-2 text-blue font-bold border-r border-gray-300"
            >
              Customer Code
            </td>
            <td class="w-1/4 px-4 py-2 text-lg text-blue">WHIFLO</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Sales Orders
            </td>
            <td class="px-4 py-2 text-blue">LOREM</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Delivery Date
            </td>
            <td class="px-4 py-2 text-blue">2/JAN/24</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Pieces Scheduled
            </td>
            <td class="px-4 py-2 text-blue">03</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Customer Name
            </td>
            <td class="px-4 py-2 text-blue">JON VEN</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Address
            </td>
            <td class="px-4 py-2 text-blue">USA</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Phone Number
            </td>
            <td class="px-4 py-2 text-sm text-blue">(415) 555 00</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Average Sale
            </td>
            <td class="px-4 py-2 text-blue">3,500</td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- Second Table -->

    <div class="w-full max-w-4xl rounded-xl border border-[#D9D9D9] p-2 mt-8">
      <table class="w-full table-auto">
        <tbody>
          <tr>
            <td
              class="w-3/4 px-4 py-2 text-blue font-bold border-r border-gray-300"
            >
              Customer Code
            </td>
            <td class="w-1/4 px-4 py-2 text-lg text-blue">WHIFLO</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Sales Orders
            </td>
            <td class="px-4 py-2 text-blue">LOREM</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Delivery Date
            </td>
            <td class="px-4 py-2 text-blue">2/JAN/24</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Pieces Scheduled
            </td>
            <td class="px-4 py-2 text-blue">03</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Customer Name
            </td>
            <td class="px-4 py-2 text-blue">JON VEN</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Address
            </td>
            <td class="px-4 py-2 text-blue">USA</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Phone Number
            </td>
            <td class="px-4 py-2 text-sm text-blue">(415) 555 00</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-2 text-blue font-bold border-r border-gray-300">
              Average Sale
            </td>
            <td class="px-4 py-2 text-blue">3,500</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showCurrentWeek: true // Initial state to show the current week
    };
  },
  methods: {
    toggleWeek() {
      this.showCurrentWeek = !this.showCurrentWeek; // Toggle the state
    }
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Jost:wght@400;700&display=swap");
</style>
