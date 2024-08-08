<template>
  <div class="bg-white p-7 shadow-xl rounded-3xl">
    <div class="py-2 text-[#00555D] font-extrabold text-2xl">
      Bear's Email
    </div>
    <div class="py-1 px-4 text-[#00555D] text-lg bg-[#F6F6F6] rounded-full w-fit">
      All Email
    </div>

    <div class="mt-6">
      <!-- User 1 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Ryan R. Hinds</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">18.31</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">09</div>
          </div>
        </div>
      </div>

      <!-- User 2 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2-3.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Amanda L. Townsend</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">19.24</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">02</div>
          </div>
        </div>
      </div>

      <!-- User 3 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2-1.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Royce A. Jorgensen</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">20.38</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">08</div>
          </div>
        </div>
      </div>

      <!-- User 4 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2-4.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Elvie J. Juarez</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">17.47</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">01</div>
          </div>
        </div>
      </div>

      <!-- User 5 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2-2.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Joseph P. Williams</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">10.26</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">06</div>
          </div>
        </div>
      </div>

      <!-- User 6 -->
      <div class="flex items-center justify-between mt-8">
        <img class="w-24 h-24" src="/src/assets/images/ellipse-2-5.png" />
        <div class="ml-2 w-2/3">
          <p class="text-2xl font-bold text-blue">Clara C. Casper</p>
          <p class="text-blue text-sm font-normal text-wrap">
            Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="flex flex-col items-center ml-auto">
          <div class="text-black text-sm font-medium mt-1">05.50</div>
          <div class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center">
            <div class="text-white text-sm font-bold">03</div>
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
      users: [
        {
          name: 'Ryan R. Hinds',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '18.31',
          number: '09',
          image: '/src/assets/images/ellipse-2.png'
        },
        {
          name: 'Amanda L. Townsend',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '19.24',
          number: '02',
          image: '/src/assets/images/ellipse-2-3.png'
        },
        {
          name: 'Royce A. Jorgensen',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '20.38',
          number: '08',
          image: '/src/assets/images/ellipse-2-1.png'
        },
        {
          name: 'Elvie J. Juarez',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '17.47',
          number: '01',
          image: '/src/assets/images/ellipse-2-4.png'
        },
        {
          name: 'Joseph P. Williams',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '10.26',
          number: '06',
          image: '/src/assets/images/ellipse-2-2.png'
        },
        {
          name: 'Clara C. Casper',
          description: 'Lorem ipsum dolor sit amet, consectetur elit do eiusmod tempor incididunt.',
          time: '05.50',
          number: '03',
          image: '/src/assets/images/ellipse-2-5.png'
        },
      
        // Add more user objects as needed.
      ]
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@600&family=Jost:wght@400;500;700&display=swap");
</style>
