<template>
  <div class="bg-white p-7  shadow-xl rounded-3xl">

    <div class=" py-2 text-[#00555D] font-extrabold text-2xl">
        Bear's Email
      </div>
      <div class=" py-1 px-4 text-[#00555D]  text-lg bg-[#F6F6F6] rounded-full w-fit">
        All Email
      </div>


<div class="mt-6">
    <!-- <div class="flex items-center justify-between">
      <img
        class="w-24 h-24"
        alt="Ellipse"
        src="/src/assets/images/ellipse-2.png"
      />

      <div class="ml-2">
        <p class="text-2xl font-bold text-blue">Ryan R. Hinds</p>
        <p class="text-blue text-sm font-normal ">
          Lorem ipsum dolor sit amet, consectetur adipisc<br />
          ing elit sed do eiusmod tempor ncididunt.
        </p>
      </div>

      <div class="flex flex-col items-center ml-auto">
        <div class="text-black text-sm font-medium mt-1">18.31</div>
        <div
          class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center"
        >
          <div class="text-white text-sm font-bold">09</div>
        </div>
      </div>
    </div> -->


    <div class="">
    <div v-for="(user, index) in users" :key="index" class="flex items-center justify-between  mt-8">
      <img
        class="w-24 h-24"
        :alt="user.name"
        :src="user.image"
      />

      <div class="ml-2 w-2/3">
        <p class="text-2xl font-bold text-blue">{{ user.name }}</p>
        <p class="text-blue text-sm font-normal text-wrap">
          <span v-html="formatDescription(user.description)"></span>
        </p>
      </div>

      <div class="flex flex-col items-center ml-auto">
        <div class="text-black text-sm font-medium mt-1">{{ user.time }}</div>
        <div
          class="h-8 w-8 rounded-full bg-gradient-to-b from-cyan-700 to-blue-900 shadow-lg flex items-center justify-center"
        >
          <div class="text-white text-sm font-bold">{{ user.number }}</div>
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
  methods: {
    formatDescription(description) {
      return description.replace(/\n/g, '<br />');
    }
  }
};
</script>



<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@600&family=Jost:wght@400;500;700&display=swap");
</style>
